# Guide: research-notion

**For:** anyone who needs a researched, cited answer and wants it saved as a Notion page they can review, not a chat that scrolls away.

## What it does

Runs research as three approval-gated steps: **Brief → Plan → Execute**. Each research becomes a page in your **Kutatások** area, with the Brief and Plan as subpages. Claude does not start the next step until you say "approved".

## Before you start

- The Notion connector is enabled and has access to your Kutatások page.
- Decide where Claude may look: **Notion only**, **public internet only**, or **hybrid**. You choose this in the brief.

## Scenario: "Should our team adopt a heat-pump subsidy scheme for the office renovation?"

Maya is a facilities manager. She has two weeks and needs a short, sourced report.

**1. Start**

> Start a new research: heat-pump subsidies for office buildings in Hungary, and put it in Kutatások.

Claude first searches your existing researches for overlap and shows close matches. If one already covers the topic, it offers to extend that one instead. Otherwise you carry on.

**2. Brief (you fill in the details)**

Claude walks you through the fields in small groups:

- target questions (e.g. "Which subsidies exist for offices over 500 m²?", "What is the payback period at current energy prices?")
- in scope / out of scope (out of scope: residential schemes)
- research area: hybrid (your Notion notes plus the web)
- allowed or banned sources (e.g. only government and standards bodies)
- length limits (e.g. executive summary about 200 words)

Claude proposes a title and a REF number (highest found plus one). It creates the research page and the Brief subpage, then gives you the link. **Edit the page directly in Notion if you like**, then reply "approved".

**3. Plan**

Claude writes the Plan subpage from the approved brief: how it will answer each question and which sources it will check. Review, edit, approve.

**4. Execute**

Claude researches within the approved scope and publishes the cited report on the research page. Status moves to `Kész`.

**5. Afterwards**

- Ask a question across everything you have researched: *"What did my past researches say about energy costs?"* (`research-query`, read-only)
- Update it later: *"Refresh REF-0047 with 2027 subsidy rules."* (`research-extend`, with your approval)
- Turn it into lasting notes: *"Make zettels from this research."* (`research-to-zettel`)

## Zettelkasten step

`research-to-zettel` proposes 5–12 atomic notes (one idea each, with links and the Map of Contents they belong to) as a table. Nothing is written until you approve. New zettels are titled `YYYYMMDDHHMM Name`.

## Tips

- Be concrete in **out of scope**. It is the main guard against wandering.
- Journal areas (Napló, Gondolatok) are excluded unless you name them.
- Documents are in English; labels and statuses are in Hungarian.

## Good to know

- Claude cannot delete Notion pages. Retired pages get a `[removed] ` title prefix.
- Say "where am I with my research?" at any time to resume or see the next gate.
