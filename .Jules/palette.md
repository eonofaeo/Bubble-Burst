
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.
## 2026-08-14 - Visually hidden elements and keyboard focus
**Learning:** Using `pointer-events: none` and `opacity: 0` to visually hide elements does not prevent them from receiving keyboard focus (e.g., via the `Tab` key), which can confuse screen readers and keyboard users.
**Action:** Always include `visibility: hidden` (or `display: none`) when hiding elements to ensure they are fully removed from the accessibility and focus tree.
