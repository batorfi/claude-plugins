# Guide: educator-notion

**For:** students and self-learners who want a tutor that helps them *understand and solve things themselves*, and that remembers where they stand.

## What it does

A personal educator that:

- **explains** at your level (`educator-explain`)
- **coaches** you through problems with a hint ladder instead of giving answers (`educator-coach`)
- **writes how-to guides** for unfamiliar processes (`educator-howto`)
- **assesses** what you know and where the gaps are (`educator-assess`)
- **links** everything you create into a knowledge web (`educator-weave`)

It knows you through a **learner profile**, a **Sessions** history and a **Knowledge** database in your Notion, plus the course materials you provide.

## Before you start

- The Notion connector is enabled.
- Run `educator-setup` once (profile, databases, course pages). You can still ask questions before setup; it will offer setup afterwards.

## Scenario: a linear algebra exam in three weeks

Bence is a second-year engineering student. He struggles with eigenvalues.

**1. Setup**

> Set up my educator hub. I'm studying Linear Algebra at BME; here's the syllabus.

Claude builds the hub, a Course page with a materials map, and asks about your preferences (including an **answer policy**: how much it may reveal).

**2. Find where you stand**

> Where am I with eigenvalues? Test me.

`educator-assess` runs an adaptive diagnostic and finds prerequisite gaps (say, determinants). It updates your knowledge model.

**3. Learn the concept**

> Explain eigenvalues.

You get a layered explanation calibrated to your level. Claude offers a **Concept card** page; it writes one only if you say yes.

**4. Solve a problem**

> Help me with exercise 5 from the problem sheet.

Claude asks for **your attempt first**, then gives one small hint at a time (restate the problem, then a pointer, and so on). If you ask for the solution, it first offers another nudge or a worked analogue. For graded or exam work it never solves it for you.

**5. Wrap up**

At the end Claude summarises what was covered and asks "Shall I log this session?", showing the proposed updates (for example *Eigenvalues: Introduced → Practising*). It offers a **Problem journey** page and proposes where to link it.

## Tips

- Say what the work is for (practice, graded, exam). It changes how much help you get.
- A mastery level rises only on two independent signals, so progress is evidence-based.
- For a long-term plan, flashcards and spaced review, it hands off to **learn-notion**.

## Good to know

- Learner data lives only in your Notion hub.
- Pages and logs are proposed first. It never deletes or moves anything.
