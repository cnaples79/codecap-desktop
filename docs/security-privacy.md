# Security & Privacy — CodeCap (Desktop MVP)

## Principles
- **Privacy by default:** Only the extracted text is persisted by default; raw images are discarded unless user opts in for troubleshooting.
- **Local-first:** Content is stored locally (SQLite) in the MVP. Cloud sync is out of scope.
- **Transparency:** Users can see and control AI settings (provider, API key).

## Data Handling
- **At rest:** Plan to encrypt snippet content with an app-level key (implementation TBD).
- **In transit:** If AI is enabled, text is sent to the chosen provider over HTTPS.
- **Logging:** No sensitive content in logs. Optional, anonymized telemetry only.

## AI
- Users can disable AI entirely.
- When enabled, summaries/tags are generated; content is retained locally.

## Permissions
- Screen capture permission (OS-specific) is required for the Cap tool.
- Clear in-app cues (overlay, crosshair cursor) indicate when capture is active.
