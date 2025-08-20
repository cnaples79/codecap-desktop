# UX Flows — CodeCap (Desktop MVP)

## Tray → Emblem → Toolbar
1. User clicks the **system tray** icon.
2. A **floating emblem** appears: a rectangular badge with cursive “CC”.
3. User clicks the emblem → **vertical toolbar** expands (narrow, hover-tooltips).
   - Top to bottom: **Codes**, **Cap**, **AI**, **Settings**.

## Capture (Cap) Flow
1. User clicks **Cap** (or presses global hotkey).
2. Desktop dims with a translucent **grey overlay**; cursor becomes a crosshair.
3. User clicks and drags to define a **selection rectangle** (pixel dims visible).
4. On release:
   - Region is captured as an image.
   - OCR converts image → text (preserve whitespace/indentation).
   - A **post-capture modal** opens with extracted text and fields: title, category (code / acceptance criteria / notes), tags.
   - AI runs (if enabled) to summarize and suggest tags.
5. Save snippet → appears in **Codes**.

## Codes View
- Search box; filter by tag, category, language (for code).
- Items show title, preview, tags, created/updated dates.
- Quick actions: **Copy**, **Open details**, **Favorite**.

## AI View
- Settings for summarization and tag suggestions.
- Manual run: select a snippet → **Analyze** for summary or hints.

## Settings View
- Shortcuts (global cap hotkey).
- OCR language packs.
- Privacy: keep/discard raw images after OCR; allow/disable cloud AI calls.
- Theme: black/white/grey with blue accents.
