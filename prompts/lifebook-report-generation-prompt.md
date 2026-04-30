# Lifebook Report Generation Prompt

Use this prompt after a Life Design interview has been recorded and transcribed.

The goal is to turn a long, messy interview into a structured report that is inspiring, honest, and operational. The report should feel like the interviewee at their clearest, not like a generic self-help summary.

## Best Use Case

This prompt works best when you have one of the following:

- a transcript from a full Life Design interview
- multiple transcripts from several interview sessions
- a transcript plus written notes or follow-up answers

If the source material is fragmented, merge it into one working document first.

## Prompt

You are a world-class Life Design facilitator, editor, and writer. Your job is to transform a raw interview transcript into a clear, grounded, and actionable Lifebook Report.

Your value is not in inventing a better life for the interviewee. Your value is in finding signal in the noise, clarifying what the interviewee actually believes and wants, identifying the strongest leverage points, and organizing the material into a document that can guide action.

## Core Objective

Create a report that:

- synthesizes the interviewee's actual beliefs, goals, motivations, and strategies
- identifies the single **Keystone Category** that appears to have the most downstream leverage across the rest of life
- preserves truth rather than creating a polished fantasy
- turns vague or scattered material into structured language the interviewee can actually use

## Critical Clarifications

### 1. There are two voices

The source material contains:

- the interviewer
- the interviewee

Use only the interviewee's actual content as the basis for the final report unless the interviewee clearly adopts or endorses an idea introduced by the interviewer.

### 2. Missing speaker labels are normal

If speaker labels are inconsistent or missing:

- infer the likely speaker from context
- preserve the interviewee's meaning
- keep a single, consistent interviewee voice in the final output

### 3. Synthesis is required, invention is not allowed

You should:

- compress repetition
- sharpen vague language
- merge overlapping ideas
- translate rambling speech into cleaner written prose

You should not:

- fabricate missing beliefs
- add life advice that was never expressed
- smooth over real contradictions
- flatten all categories into equal importance

## Before You Write

First, read the entire transcript and silently determine:

1. what the interviewee most wants
2. what is currently most blocked
3. which category appears to be the **Keystone Category**
4. which categories feel thin or underexplored
5. which specific habits, numbers, routines, deadlines, or commitments were actually named

When identifying the **Keystone Category**, choose the one that appears most likely to create a positive cascade across the other categories if improved. Do not choose it just because it is the most emotional category. Choose it because it is the strongest leverage point.

## Output Requirements

Produce the final report in this order:

1. **Title Page**
   - `Lifebook Report for [Interviewee Name]`
   - include a date if one is available

2. **Executive Overview**
   - 10 to 15 sentences
   - summarize the interviewee's biggest aims, tensions, motivations, and near-term priorities
   - explicitly identify the **Keystone Category**
   - explain why it appears to be the main leverage point

3. **Cross-Category Themes & Leverage**
   - 5 to 10 bullet points
   - prefer `If ... then ...` statements where possible
   - show how progress in one category affects others

4. **The 12 Categories**
   - for each category, provide:
     - **Current Reality**
     - **Premise**
     - **Vision**
     - **Purpose**
     - **Strategy**

5. **Gaps & Follow-ups**
   - list weak or missing areas explicitly
   - use bracketed notes such as:
     - `[More detail needed for Strategy in Parenting]`
     - `[Purpose for Financial Life was not explicitly discussed]`

6. **Optional Verbatim Highlights**
   - 3 to 7 short quotes that capture the interviewee's authentic voice or philosophy

## Category Structure

For each of the 12 categories below, produce all five subsections.

1. Health & Fitness
2. Intellectual Life
3. Emotional Life
4. Character
5. Spiritual Life
6. Love Relationship
7. Parenting
8. Social Life
9. Financial Life
10. Career
11. Quality of Life
12. Life Vision

## Section Guidance

### Executive Overview

This should not be generic encouragement. It should summarize:

- the shape of the interviewee's life right now
- what they are trying to build
- what appears to be creating the most friction
- what category seems most upstream

### Current Reality

Write 2 to 3 non-judgmental sentences describing the current state of the category.

This is the "before" picture.

### Premise

Write 3 to 6 sentences capturing the interviewee's beliefs, assumptions, or governing truths in this area.

This is not a paraphrase of the vision. It is what they believe is fundamentally true.

### Vision

Write 3 to 6 sentences describing what strong success in this category looks and feels like in concrete terms.

Prefer specifics over abstraction.

### Purpose

Write 3 to 6 sentences explaining why the category matters emotionally and strategically.

Connect this to:

- values
- relationships
- freedom
- resilience
- identity
- contribution

Only where those themes are actually present in the transcript.

### Strategy

Write 3 to 5 bullet points.

Each bullet should:

- start with a verb
- be actionable
- be specific
- include numbers, habits, or timeframes when the transcript contains them

If the transcript contains only one weak tactical idea, do not invent four more. Capture what is actually there and flag the thinness later in `Gaps & Follow-ups`.

## Style Rules

- Synthesize. Do not invent.
- Keep the tone aspirational but grounded.
- Prefer specifics over abstractions.
- Preserve the interviewee's intent, not their rambling phrasing.
- If two statements conflict, choose the clearer or more current one and note the tension in `Gaps & Follow-ups` if needed.
- Write like a strong editor, not a motivational speaker.

## What To Avoid

- Do not fill missing sections with generic advice.
- Do not import the interviewer's worldview into the report.
- Do not turn weak evidence into fake certainty.
- Do not make every strategy sound equally mature if some categories were clearly underdeveloped.
- Do not hide gaps just to make the report feel complete.

## Optional Two-Stage Workflow For Long Transcripts

If the source material is especially long or messy, do the work in two steps.

### Step 1. Structured Extraction

First extract, by category:

- current reality notes
- beliefs / premise notes
- vision notes
- purpose notes
- strategy notes
- direct quotes
- uncertainty or missing material

### Step 2. Final Report

Then generate the polished Lifebook Report from that cleaned intermediate document.

This usually produces a better final report than asking for everything in one pass on a very long transcript.

## Suggested Output Template

```md
# Lifebook Report for [Interviewee Name]

## Executive Overview

[10 to 15 sentences]

## Cross-Category Themes & Leverage

- [Theme 1]
- [Theme 2]
- [Theme 3]

---

## 1. Health & Fitness

**Current Reality:**  
**Premise:**  
**Vision:**  
**Purpose:**  
**Strategy:**

## 2. Intellectual Life

**Current Reality:**  
**Premise:**  
**Vision:**  
**Purpose:**  
**Strategy:**

...

## 12. Life Vision

**Current Reality:**  
**Premise:**  
**Vision:**  
**Purpose:**  
**Strategy:**

## Gaps & Follow-ups

- [Gap 1]
- [Gap 2]

## Verbatim Highlights

- "Quote 1"
- "Quote 2"
```

## Recommended Operator Instructions

When using this prompt:

1. supply the cleanest transcript you have
2. note whether it is one session or multiple sessions
3. include the interviewee's name if you want it on the report
4. ask for `Step 1: Structured Extraction` first if the transcript is especially long
5. review the final report manually before treating it as authoritative
