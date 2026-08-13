
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.

## 2026-08-10 - Hidden Element Keyboard Focus Trap
**Learning:** Using only `opacity: 0` and `pointer-events: none` to hide UI elements (like the game HUD) does not remove them from the keyboard tab order. This creates a confusing experience for screen reader and keyboard users who can focus on invisible, inactive buttons.
**Action:** Always combine `visibility: hidden` with `opacity` transitions when animating elements out of view to ensure they are properly removed from the accessibility tree and keyboard navigation flow.
