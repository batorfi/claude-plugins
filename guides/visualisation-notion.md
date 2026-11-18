# Guide: visualisation-notion

**For:** anyone who needs consistent, on-brand visuals (infographics, diagrams, slide graphics) and will produce them in Claude Design or with a designer.

## What it does

It **does not draw**. It writes the specification: a design-system digest, a set overview, and one concept page per visual with composition, exact content, two variants, accessibility notes and a **paste-ready Claude Design prompt**. Flow: **Brief (+ digest) → Plan → Make**, approval at each gate.

## Before you start

- The Notion connector is enabled.
- A design-system source: a Notion page, pasted tokens, or a file.
- Know the data or message each visual must carry.

## Scenario: five graphics for an annual-report presentation

Lena works in communications. Her company has a brand guide in Notion and she needs five visuals: a timeline, two charts, a process diagram and a cover graphic.

**1. Start**

> Create visualisation concepts for our annual report deck. Brand guide is on this Notion page: <link>.

**2. Brief and design-system digest**

Claude collects the audience, usage context and locations. It then reads your brand guide and writes a **Design system digest**: colour roles, type scale, spacing, chart style, plus **contrast checks** and a list of **gaps** (things the guide doesn't define). It never invents a colour or font. You approve the Brief and the digest together.

**3. Plan**

A visual inventory (what each visual is for, its type) and consistency rules shared across the set. Approve.

**4. Make**

With more than three concepts, Claude writes a **pilot** concept first. You approve the pilot, then it writes the rest. Each concept page ends with a prompt block to copy into Claude Design.

**5. After**

- `visualisation-critique`: checks the set against the digest, perception and accessibility rules, and prompt quality.
- `visualisation-revise`: *"Make the timeline vertical and add a dark variant."*
- The digest is reusable. Next set, link the existing one instead of rebuilding it.

## Tips

- Supply real numbers. Gaps are marked `[NEEDS: …]`.
- If the digest flags low contrast on your accent colour, it proposes a fix but never applies it without your approval.
- Anything beyond the approved tokens appears as a labelled extension proposal.

## Good to know

- Handoff to Claude Design is manual: copy the prompt blocks.
- Documents in English; chat follows your language.
