# Tracked Metrics Template

This file is a sanitized starting point for turning monthly Life Design ratings into a Dataview-based dashboard in Obsidian.

It assumes that monthly review notes live in a `Monthly` folder and contain frontmatter or inline fields for the 12 rating categories.

## Year / Month / Day Progress

```dataviewjs
const now = new Date();
const startOfYear = new Date(now.getFullYear(), 0, 1);
const endOfYear = new Date(now.getFullYear() + 1, 0, 1);
const dayOfYear = Math.floor((now - startOfYear) / (24 * 60 * 60 * 1000)) + 1;
const weekOfYear = Math.ceil(dayOfYear / 7);
const yearProgress = ((now - startOfYear) / (endOfYear - startOfYear)) * 100;

dv.table(
  ["Day of Year", "Week of Year", "Year Progress"],
  [[dayOfYear, weekOfYear, yearProgress.toFixed(2) + "%"]]
);
```

## Life Design Log

```dataviewjs
dv.span("**Life Design Log**");

const requiredVariables = [
  "health_fitness_life_rating",
  "intellectual_life_rating",
  "emotional_life_rating",
  "character_life_rating",
  "spiritual_life_rating",
  "love_relationships_life_rating",
  "parenting_life_rating",
  "social_life_rating",
  "financial_life_rating",
  "career_life_rating",
  "quality_of_life_rating",
  "life_vision_rating"
];

const pages = dv.pages('"Monthly"')
  .where(p => requiredVariables.some(v => p[v] !== undefined) && p.date)
  .sort(p => p.date.toISODate());

const dates = pages.map(p => p.date.toISODate());

const getOrDefault = (page, key) => {
  const value = page[key];
  return value !== undefined && value !== null && value !== "" ? value : 0;
};

const ratings = {
  health_fitness_life_rating: [],
  intellectual_life_rating: [],
  emotional_life_rating: [],
  character_life_rating: [],
  spiritual_life_rating: [],
  love_relationships_life_rating: [],
  parenting_life_rating: [],
  social_life_rating: [],
  financial_life_rating: [],
  career_life_rating: [],
  quality_of_life_rating: [],
  life_vision_rating: []
};

pages.forEach(page => {
  for (const key of Object.keys(ratings)) {
    ratings[key].push(getOrDefault(page, key));
  }
});

window.renderChart({
  type: 'line',
  data: {
    labels: dates,
    datasets: [
      { label: 'Health', data: ratings.health_fitness_life_rating },
      { label: 'Intellectual', data: ratings.intellectual_life_rating },
      { label: 'Emotional', data: ratings.emotional_life_rating },
      { label: 'Character', data: ratings.character_life_rating },
      { label: 'Spiritual', data: ratings.spiritual_life_rating },
      { label: 'Love', data: ratings.love_relationships_life_rating },
      { label: 'Parenting', data: ratings.parenting_life_rating },
      { label: 'Social', data: ratings.social_life_rating },
      { label: 'Financial', data: ratings.financial_life_rating },
      { label: 'Career', data: ratings.career_life_rating },
      { label: 'Quality', data: ratings.quality_of_life_rating },
      { label: 'Vision', data: ratings.life_vision_rating }
    ]
  },
  options: {
    responsive: true,
    scales: {
      y: {
        min: 0,
        max: 10
      }
    }
  }
});
```

## Notes

- This is intentionally generic.
- If you want life-countdown widgets, add them separately and keep personal birth dates private.
- The point of the dashboard is not false precision. The point is trend visibility across months.
