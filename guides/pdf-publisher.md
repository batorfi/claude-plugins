# Guide: pdf-publisher

**For:** anyone who needs a polished, branded PDF (report, proposal, handbook, print-ready booklet) built from local files or Notion pages.

## What it does

Builds PDFs with a bundled local Python engine (WeasyPrint, pikepdf), styled by **your design system**. Flow, with an approval gate at every step:

**Brief → Design (specimen) → Plan → Make (draft, then final) → Review**

Features include cover, table of contents, running headers and footers, page numbering per part, watermarks, mixed orientation, columns, bleed and crop marks, bookmarks, PDF/A, PDF/UA and PDF/X, encryption, and versioning with a changelog.

## Before you start

- Python 3.10+, a virtual environment, and `pip install -r skills/pdf-publish/engine/requirements.txt` inside the plugin. On macOS also `brew install pango`. Claude asks before installing anything.
- Optional extras: poppler (image resolution check), mermaid-cli, Ghostscript, veraPDF (standards validation), Ollama (reading reference images).
- Notion sources: set `NOTION_TOKEN` in your environment **outside the chat** (otherwise pages are staged through the connector). PDF passwords go in `PDF_OWNER_PASSWORD` / `PDF_USER_PASSWORD`, never typed in the chat.
- Your design system as a Notion page, `DESIGN.md`, a tokens JSON, CSS, or a Claude Design export.

## Scenario: a client-ready annual report from a folder of drafts

Karolina is a finance manager. She has Markdown chapters, a few Word files and a brand guide in Notion. The board wants a print-ready PDF.

**0. Environment check**

Claude runs a doctor check and reports in plain language what works and what is missing (say, no veraPDF, so standards can't be validated).

**1. Brief**

Claude asks about:

- purpose and audience (printed for the board, also emailed)
- sources (folder paths, order, Notion pages)
- content mode: **Compose** (Claude condenses or writes text, with gaps as `[NEEDS: …]`) or **Typeset** (your text used as-is)
- page setup (A4, mirrored margins for binding), cover, TOC depth, headers and footers, page numbering (roman front matter, arabic body)
- a watermark (DRAFT by default on the first build)
- quality target (screen, print or archival) and output folder

You approve the brief, which is saved as `brief.md`.

**2. Design and specimen**

Claude reads your brand guide and shows: colours by role, requested vs chosen fonts (and whether they may be embedded and cover Hungarian ő/ű), the print type scale, **contrast findings** and **proposals**. You decide each proposal. The design is applied as stated, and nothing changes without your yes. It then builds a **specimen PDF** (cover, TOC, callouts, table, a landscape page) for approval.

**3. Plan**

Sources are staged, and Claude proposes the outline, per-part layout and feature checklist. It writes `build.json` and waits for approval.

**4. Make**

A **draft** with the DRAFT watermark first. Claude looks at the rendered pages itself and tells you what it sees. You review it, then it builds the **final**.

**5. Review**

`ENGINE qa` checks run and a `qa-vN.md` report is written. Any later change (new text, new theme) produces a **new version** (`-v2`, `-latest`) with a changelog. Nothing is overwritten.

## Tips

- Run the specimen before the content. Font and contrast problems show up in a minute instead of after 80 pages.
- A final can't be published while `[NEEDS: …]` placeholders remain.
- Fonts with restrictive embedding licences (for example Futura on macOS) are skipped for the next font in your stack. You may allow one for a private PDF, but the licence still applies if you share it.

## Good to know

- Notion is **read-only** for this plugin.
- Tested with mock services. Run the specimen and a draft before relying on a final.
- `python3 skills/pdf-publish/engine/selftest.py` runs 25 self-checks.
