
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.

## 2026-08-21 - Better Accessibility for Toggle Buttons
**Learning:** For toggle buttons (like mute/unmute), rather than dynamically changing the `aria-label` which can confuse screen readers, it is better to use a static `aria-label` that describes the purpose of the button (e.g., "Mute sound"), and dynamically update the `aria-pressed` attribute (`true` or `false`) to indicate the current state.
**Action:** Use static `aria-label` and dynamic `aria-pressed` attributes for all toggle buttons moving forward.
