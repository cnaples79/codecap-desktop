# Testing Plan — CodeCap (Desktop MVP)

## Manual Test Checklist
- **Tray/Emblem/Toolbar**
  - Tray icon appears on launch.
  - Emblem shows/hides, toolbar expands/collapses.
- **Capture**
  - Hotkey opens grey overlay and crosshair cursor.
  - Selection rectangle works on single and dual monitors.
  - ESC cancels; Enter confirms.
- **OCR**
  - Extracts basic text and preserves indentation for code samples.
  - OCR language selection affects recognition quality.
- **AI (optional)**
  - Summary and tag suggestions render for a sample snippet.
  - Disabling AI prevents external calls.
- **Codes**
  - Create snippet from capture; edit title/tags/category.
  - Search and filter return expected results.
  - Copy to clipboard works.
- **Settings**
  - Update and persist hotkeys, theme, privacy flags.
  - Toggle “keep raw images” and confirm behavior.

## Automated Testing (to be added)
- Unit tests for IPC handlers (mocked).
- Worker tests for OCR pipeline (mocked images).
- Snapshot tests for renderer views.

## Performance Checks
- CPU/memory usage during capture and OCR.
- Responsiveness of UI during worker tasks.
