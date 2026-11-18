# Guide: learn-notion

**For:** self-paced learners who want a structured path, daily lessons, quizzes and spaced-repetition review, tracked in Notion.

## What it does

Claude teaches; Notion stores everything in a **Learning** hub with six databases: Paths, Modules, Lessons, Quizzes, Flashcards and Journal. Say `/learn` or "I want to learn X".

## Before you start

- The Notion connector is enabled.
- Run `learn-setup` once to build the hub.
- Migrating from the old file-based PPW tool? Use `learn-import`, with the PPW folder linked to the session.

## Scenario: learn SQL in six weeks, 30 minutes a day

Nora is an analyst who wants to stop asking colleagues for data pulls.

**1. One-time setup**

> Set up my learning hub.

**2. Create a path**

> I want to learn SQL.

Claude collects four things in one message: **specific topic** ("SQL for analytics", not "SQL"), **level** (beginner / advanced / mastery), **daily time** and **total duration**. It checks what you already know, then shows an outline of modules and lessons and asks you to confirm before creating the path.

**3. Learn daily**

> Continue my SQL path.

Claude opens with a short recap if you've been away, mentions reviews due, then teaches the current lesson. When you answer the check question correctly it marks the lesson done and creates 3–5 **flashcards** due tomorrow.

**4. Quiz and review**

> Quiz me on module 1.

Questions come one at a time with feedback. At 70% or above it suggests moving on; below, it names weak areas and won't advance. Lessons are reviewed 1, 3, 7 and 30 days after completion; flashcards use their own 1/3/7/30/90-day ladder. Ask "what's due?" to run reviews.

**5. Stuck?**

> I don't get JOINs.

Claude helps and logs a **struggle** in the Journal. After three or more struggles it offers an analysis of the pattern.

**6. Status**

> How am I doing?

## Handy Notion views

Lessons → **Review queue**, **Board** · Flashcards → **By due date**, **Calendar** · Journal → **Struggles**.

## Tips

- Pick a narrow topic. Broad ones create vague paths.
- You can pause, resume or modify a path at any time.
- At the end, ask it to turn key insights into zettels.

## Good to know

- Claude recomputes progress from lesson statuses, because the connector can't read formula or rollup values.
- "Remove" marks pages Skipped and `[removed]`, since pages can't be deleted.
