
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.

## 2026-08-18 - HUD Button Keyboard Trap
**Learning:** Elements hidden with `opacity: 0` and `pointer-events: none` remain in the DOM and are still focusable via keyboard navigation (Tab key). This creates a "keyboard trap" where users can focus invisible elements, leading to a confusing experience.
**Action:** When hiding interactive containers (like the HUD), always use `visibility: hidden` (or `display: none`) alongside `opacity: 0`. Added `visibility: hidden` to `#hud.hide` and updated its transition.
