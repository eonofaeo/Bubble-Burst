
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.

## 2026-08-22 - Add ARIA pressed state to toggle buttons
**Learning:** Screen readers and accessibility tools rely on `aria-pressed` for toggle buttons rather than updating the `aria-label` dynamically, which can be confusing.
**Action:** Use a static `aria-label` (e.g., `aria-label="Toggle mute"`) and update `aria-pressed` to `true` or `false` based on the active state.
