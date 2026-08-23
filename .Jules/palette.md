
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.

## 2026-08-09 - Use static aria-label and aria-pressed for toggle buttons
**Learning:** For toggle buttons (like mute/unmute), it is better for accessibility to use a static `aria-label` (e.g., "Toggle mute") and dynamically update the `aria-pressed` attribute, rather than dynamically changing the `aria-label` itself to indicate state.
**Action:** Always use `aria-pressed` for toggle buttons to provide clear state changes to screen readers while keeping the button's identity stable.
