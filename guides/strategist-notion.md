# Guide: strategist-notion

**For:** people who must recommend a direction and defend it with evidence: managers, founders, consultants, analysts.

## What it does

Acts as a strategic advisor. From your end-state and outcomes it builds a fact-based strategy as Notion pages: an answer-first executive summary, diagnosis, options and their evaluation, the recommended strategy, roadmap, KPIs, risks and decisions. It also produces a **fact pack**, an **Evidence database**, an **Initiatives database** and visuals (SVG charts, Mermaid diagrams).

Flow: **Brief → Plan → Make**, with a **findings checkpoint** before the recommendation is written.

## Before you start

- The Notion connector is enabled (database and attachment tools are used too).
- Know your **end-state** (where you want to be, by when) and your constraints. If these are unclear, Claude will ask rather than guess.
- Decide whether web research is allowed. Optional: Python 3 for the bundled chart script.

## Scenario: a regional bakery chain deciding how to grow

Anna owns six bakeries. She wants to double revenue in three years without losing margin.

**1. Start**

> Build a strategy: double revenue in 3 years for my bakery chain, keeping margin above 12%.

**2. Brief**

Claude collects context, end-state, outcomes (each with a baseline, target and KPI), constraints (cash, staff), decision criteria, internal sources it may read (e.g. a Notion page with your sales data) and locations. It drafts a **problem statement** you must approve.

**3. Plan**

An issue tree, hypotheses, the frameworks it will use, the analysis and research plan, and the list of visuals. Approve.

**4. Make**

1. **Evidence**: facts, estimates and assumptions go into the Evidence database, each with source, date and confidence.
2. **Diagnosis and options**: e.g. open new sites, add wholesale, launch online ordering.
3. **Findings checkpoint**: Claude shows key insights and the shortlisted options and waits for your reaction. You can say "drop wholesale" here, before the recommendation is written.
4. **Strategy, roadmap, KPIs, risks** and the visuals.

Every number carries an evidence ID. Unsupported figures appear as `[NEEDS: …]` or as labelled estimates with a method.

**5. After**

- `strategist-critique`: a red-team review against consultancy standards.
- `strategist-revise`: *"Refresh the stale facts"* or *"add a scenario where flour prices rise 20%."*
- Turn it into a deck with **storyline-notion**, or into a briefing with **authoring-notion**.

## Tips

- Confidentiality: web queries are written generically and never include your internal details.
- Say "skip checkpoints" in the brief if you want fewer stops.

## Good to know

- It supports decisions. It is not a licensed financial, legal or tax advisor.
- Internal sources are read-only and only from locations you name.
