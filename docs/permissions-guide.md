# Permissions Guide — CodeCap (Desktop MVP)

## macOS
- **Screen Recording** permission is required to capture app windows.
- Grant permission in **System Settings → Privacy & Security → Screen Recording**.
- After changes, you may need to restart CodeCap.

## Windows
- No explicit global permission prompt, but Anti-Virus/Defender policies may block screen capture in corporate environments.
- High-DPI awareness: ensure capture region matches display scaling.

## Linux
- Behavior differs between X11 and Wayland. Some desktop environments restrict global capture; Wayland often requires portal APIs or user confirmation.
- Documented limitations will be surfaced in the app if detection fails.

## Best Practices
- Always inform users when capture is active (overlay + cursor change).
- ESC to cancel; Enter to confirm during capture.
- Never capture in the background without an explicit user action.
