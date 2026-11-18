# Guide: authoring-notion

**For:** anyone who writes for work (emails, messages, documents, decks) and wants it to sound like them, tailored to the audience.

## What it does

One shared **Authoring hub** in Notion holds your identity, your communication style for four audiences (leaders, direct reports, peers, partners) and your writing preferences. Four skills use it:

| Skill | Use it to |
|---|---|
| `authoring-setup` | Create or update the hub |
| `communicate` | Draft a message in your voice |
| `write-coach` | Review a document or deck |
| `strategic-reader` | Turn material into a strategic overview |

## Before you start

- The Notion connector is enabled.
- Optional: file tools to read `.docx` / `.pptx`; otherwise paste the text.

## Scenario 1: set up the hub (once, about 10 minutes)

> Set up my authoring hub.

Claude asks where it should live, then collects your identity (name, role, competencies, professional personality), picks a style for each of the four audiences from tappable options, and asks for writing preferences (spelling variant, phrases to avoid, review focus) and default output locations. It shows a summary and creates the pages only after your yes. It stores only what you state, never guesses your style from your writing.

## Scenario 2: a delicate email to your boss

Sara must tell her director that a project will slip by three weeks.

> Write an email to my director about the project delay.

Claude asks only what is unclear: purpose, key points (new date, cause, what you need), language, attachments. It then **shows the brief and waits for your confirmation** before drafting. The draft follows your leader-audience style and ends with a clear ask. Iterate in chat, approve, and it saves a Message page in Notion. **Nothing is ever sent**: you copy it into your mail client.

## Scenario 3: review a deck before it goes out

> Review this proposal deck for clarity. It's for a client's CFO.

`write-coach` rates five dimensions (structure, clarity, tone, conciseness, completeness) as Strong / Adequate / Needs Work, with **quoted findings** and concrete suggestions, saved as a Review page. It ends with the three priority actions. Source pages change only if you approve specific fixes (it shows before/after first).

## Scenario 4: a briefing from a pile of material

> Make a strategic overview of these meeting notes for the leadership team, 1 page, direct voice.

`strategic-reader` shapes length, audience, voice and form from your request and saved preferences.

## Tips

- Name the audience type each time; it decides the tone.
- Per-project overlays can adjust tone for a particular project.
- A simple summary or quick answer doesn't need this plugin.

## Good to know

- Output language defaults to that of the source or recipient.
- Pages are never deleted; retired ones get `[removed] `.
