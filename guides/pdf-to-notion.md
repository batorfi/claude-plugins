# Guide: pdf-to-notion

**For:** anyone with PDFs (lecture notes, manuals, reports, papers) they want as clean, navigable Notion pages.

## What it does

Extracts text, tables and images **locally** with a bundled Python engine (PyMuPDF), then builds Notion pages. Long PDFs become a parent page with chapter subpages, images are uploaded and embedded, and each chapter gets `← Previous | ↑ Contents | Next →` links. For a database destination, each PDF becomes an entry with **Type** and **Tags**.

Flow: **Inspect + location (Gate 1) → Formatting (Gate 2) → Extract → Build with first-PDF preview (Gate 3) → Navigation → Verify**

## Before you start

- Python 3.10+ and `pip install -r skills/pdf-to-notion/engine/requirements.txt` (PyMuPDF, Pillow). Claude asks before installing.
- Optional: `tesseract` (with Hungarian data for Hungarian text) for scanned PDFs.
- The Notion connector, with access to the destination.
- Run it through the Claude desktop app, so the engine can reach your files.

## Scenario: 12 course PDFs into a study library database

Zoli has a folder of lecture PDFs and a Notion database called "Library" with **Type** and **Tags** properties.

**Start**

> /pdf-to-notion ~/Documents/Lectures --mode quick

Flags: `--mode quick|custom`, `--profile NAME`, `--parent <Notion URL>`, `--no-preview`.

**Gate 1: inspect and destination**

Claude lists each PDF with pages, words, images, tables and the **proposed chapter split**. It warns about scanned PDFs (OCR needed, lower fidelity). **The Notion location is always asked**: a recent or favorite page, a pasted URL, or a private draft. It checks that it can write there *before* starting. For a database, it proposes a **Type and Tags table** per PDF, preferring options the database already has. New options are created only if you approve. A duplicate check avoids importing the same PDF twice.

**Gate 2: formatting**

- **Quick run**: the "Readable" preset, with a summary to confirm.
- **Custom run**: asks every option that applies to your PDFs (heading levels, collapsible sections, callouts, colours, table style, image captions, attaching the original PDF, navigation).

Saved profiles reuse a look (`--profile NAME`).

**Gate 3: preview**

Claude builds the **first PDF only** and shows it. Approve, and the rest of the batch runs.

**Navigation and verify**

Contents and previous/next links are added (re-runnable, so you can change or remove them later). `pdf-notion-verify` compares what exists in Notion with what was built and checks links and properties.

## Tips

- Check the preview closely, especially tables and math. Layout fidelity is approximate: it reads content, not page design.
- Use `--recursive` only when you want subfolders included.
- Password-protected PDFs are skipped. It never asks for the password.

## Limits worth knowing

- Notion markdown has no image width, three heading levels, a fixed colour palette and covers by image URL only.
- Images over 20 MiB are recompressed. An original PDF over 20 MiB is not attached.
- Not in v1: summaries per page, navigation chained across PDFs, per-PDF styles.
- Licence note: PyMuPDF is AGPL / commercial. Check it suits how you distribute.
