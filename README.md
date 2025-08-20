# CodeCap (Desktop MVP – Electron)

CodeCap is a desktop-first tool for capturing code and text from *any* app using a Snagit-style region selector. It preserves formatting, organizes snippets, and applies AI to summarize and tag content. This repository currently contains **no executable code**—only structure, documentation, and placeholder files for the MVP.

## Why CodeCap?
- Capture code or text from any window (IDEs, GitHub, docs) via a drag-to-select overlay.
- Preserve indentation and formatting.
- Organize snippets with projects, tags, and categories (code / acceptance criteria / notes).
- Apply AI to summarize and suggest tags.
- Share snippets with teammates and discuss via comments (MVP-light).

## MVP Scope
- Tray icon → floating emblem (“CC”) → vertical toolbar with **Codes**, **Cap**, **AI**, **Settings**.
- **Cap**: global shortcut triggers a full-screen overlay to select a region and capture → OCR → snippet save.
- **AI**: summarization and tag suggestions (configurable provider).
- **Codes**: list, search, copy, and view details.
- **Settings**: hotkeys, OCR languages, privacy defaults, theme.
- Desktop-only (Electron). No mobile/web client in MVP.

## Architecture (high-level)
- **Electron Main**: app lifecycle, tray, windows (emblem, toolbar, capture overlay), global shortcuts, IPC handlers.
- **Preload**: secure bridged APIs for renderer (contextIsolation).
- **Renderer**: UI (emblem/toolbar, Codes, AI, Settings, modals).
- **Services**: capture (screen & crop), OCR, AI, DB, security.
- **Workers**: offload OCR/cropping to avoid UI jank.
- **Data**: local SQLite via Prisma (subject to change).

## Project Structure (selected)
See `/docs/ux-flows.md` for UX flows and `/docs/security-privacy.md` for security posture.

```
codecap-desktop/
  ├─ assets/          # icons, emblem, brand
  ├─ config/          # app-config, hotkeys, schemas
  ├─ docs/            # product-vision, ux-flows, security, testing
  ├─ src/
  │  ├─ main/         # Electron main process (stubs only)
  │  ├─ preload/      # IPC bridges (stubs only)
  │  ├─ renderer/     # UI structure (stubs only)
  │  └─ workers/      # OCR/crop workers (stubs only)
  └─ native/          # future platform-specific modules
```

## Getting Started (placeholder)
This repo is a scaffold. Implementation steps will include:
1) Initialize dependencies (Electron, bundler, Tesseract, Prisma).
2) Implement tray/emblem/toolbar windows.
3) Add capture overlay and OCR workers.
4) Wire up AI provider, persistence, and basic UI.
5) Package with electron-builder.

> **Note:** No code is present yet. This README will be updated once development begins.

## Contributing
- Open issues for questions or proposals.
- Keep privacy-by-default in mind for all contributions.

## License
To be chosen (MIT/Apache-2.0/BSD-3-Clause). See `/LICENSE` placeholder.
