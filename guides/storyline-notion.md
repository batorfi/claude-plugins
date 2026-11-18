# Guide: storyline-notion

**For:** anyone preparing a talk or deck who wants the story right *before* opening PowerPoint.

## What it does

Turns your context into a **Storyline page** (the narrative arc, beat by beat) and a **Slide guide** (slide skeleton, per-slide headline, message, visual suggestion, talk track, timing). Flow: **Brief → Plan → Make**, with a stop for your approval at each gate.

## Before you start

- The Notion connector is enabled.
- Know roughly: who the audience is, what you want them to do afterwards, and how long you have.

## Scenario: a 20-minute pitch to the board for a new customer-portal project

Daniel is a product lead. He has a rough business case and a 20-minute slot.

**1. Start**

> Build a storyline for my board presentation about the customer portal.

**2. Brief**

Claude asks for everything in one pass: audience and what they care about, the decision you want, key facts and numbers, time limit, tone, and **two Notion locations**: one for the storyline, one for the slide guide. Nothing is assumed, so you name them. Review the Brief page in Notion and approve.

**3. Plan**

Claude recommends a storytelling framework from its menu (for example a problem → stakes → solution → ask arc) and drafts the arc outline. You can accept, swap the framework, or reshape the beats. Approve.

**4. Make**

Claude writes the full arc and the slide guide. Missing data is marked `[NEEDS: …]` rather than invented, so you can see exactly what to bring.

**5. After**

- `storyline-critique`: *"Score this storyline."* It reports blocking and non-blocking issues against a rubric.
- `storyline-revise`: *"Cut it to 15 minutes and drop the competitor section."* It keeps the slide guide in sync.
- Continue into visuals with **visualisation-notion**, using the Slide guide as input.

## Tips

- The more precise the audience description ("CFO sceptical about cost, CTO supportive"), the better the arc.
- Ask for a critique before you build slides. Fixing a beat is cheaper than fixing ten slides.

## Good to know

- Documents are written in English; chat follows your language.
- Claude cannot delete pages. Retired ones get `[removed] `.
