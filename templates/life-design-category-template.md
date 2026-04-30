---
date: <% tp.date.now("YYYY-MM-DD") %>
type: life_design_category
tags:
  - life-design
---
<%*
let title = tp.file.title
if (title.startsWith("Untitled")) {
  title = await tp.system.prompt("Category title")
}
await tp.file.move("/Areas/Life Design/" + title)
%>

# <% title %>

## Quotes

## Premise

What do I believe in this area?

## Vision

What does an excellent version of this area look like?

## Purpose

Why does this matter?

## Strategy

What do I need to do?

## Habits

- 

## Notes

- 

## Mentions

```dataview
TABLE WITHOUT ID
file.inlinks AS "References",
file.cday AS "Created",
summary AS "Summary"
WHERE file.name = this.file.name
```

## Meetings

```dataview
TABLE WITHOUT ID
link(file.name) AS "Meeting",
file.cday AS "Created",
summary AS "Summary"
WHERE contains(life_design_category, this.file.name)
SORT date DESC
```
