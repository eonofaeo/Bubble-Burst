
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.
## 2024-05-25 - Icon Toggle Button Accessibility
**Learning:** When using custom icon-only toggle buttons (like the mute button), screen readers need semantic feedback about the toggle state. A simple `aria-label` is not enough.
**Action:** Use `aria-pressed="false|true"` on the button and toggle this attribute in JavaScript whenever the state changes. This causes screen readers to announce it properly as a toggle button and read out its current state.
