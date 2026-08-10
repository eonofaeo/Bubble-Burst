
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.
## 2026-08-10 - Dynamic ARIA Attributes for Icon-Only Toggle Buttons
**Learning:** For icon-only toggle buttons (like mute/unmute), static `aria-label`s are insufficient. Screen readers will misreport the button's action if the visual icon changes but the ARIA text doesn't. Furthermore, using `aria-pressed` clarifies the current state as a toggle.
**Action:** When implementing an icon-only toggle button, initialize it with `aria-pressed="false"` and an `aria-label` matching its initial action. Dynamically update both the `aria-label` (or text content) and `aria-pressed` properties in Javascript upon toggle to reflect the new state correctly.
