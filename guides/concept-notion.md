# Guide: concept-notion

**For:** anyone developing an original idea (a framework, a method, a model) from a rough thought into something solid and reusable.

## What it does

Each concept is a page in a **Concept library** database. It grows through four maturity levels: **Seed → Draft → Refined → Ready**. You confirm the brief, and you approve every maturity change. Because maturity, domain and usage are database properties, you can filter instead of digging through folders.

## Before you start

- The Notion connector is enabled.
- Run `concept-setup` once. It creates the library, views and config, or adopts an existing database.
- Optional: research-notion, if you want a researched starting point.

## Scenario: a "Decision Debt" concept for a leadership workshop

Peter is an agile coach. He keeps seeing teams postpone decisions until the cost compounds, and wants to turn that into a named, teachable concept.

**1. One-time setup**

> Set up my concept library.

Claude asks where it should live and creates the database and views.

**2. Brief**

> New concept: Decision Debt.

Claude asks how to begin: **from research**, **from existing research**, **from my understanding**, or a combination. Peter picks "from my understanding". Claude checks for overlap with concepts already in the library, then asks for the brief: title, domain, core idea (a proposition, not a topic), context, and at least two key components. Optionally intended usages (training, communication, strategy). Peter confirms, and a **Seed** page is created.

**3. Develop**

> Develop it to Draft.

`concept-develop` writes the document for the current level with targeted edits. Usages you chose decide which Application Guide sections get written.

**4. Review and promote**

> Review Decision Debt: is it ready?

`concept-review` checks the criteria, stress-tests the assumptions and lists what is unmet. The gate is soft: you may promote anyway, and the override is recorded. Maturity changes only when you explicitly approve.

## Tips

- A good core idea is a claim someone could disagree with.
- Use the overlap check seriously. Linking to a related concept beats duplicating one.
- Link a concept to visuals via visualisation-notion once it is Refined.

## Good to know

- Archiving sets a property, because the connector can't delete or move pages.
- The concept's language is chosen per concept; property names and statuses are English.
