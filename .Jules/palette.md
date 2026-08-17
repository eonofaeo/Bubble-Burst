
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.
## 2026-08-17 - Global shortcuts overriding button focus
**Learning:** Global keyboard shortcuts (like Space/Enter mapped to game actions) can override native button focus functionality (Space/Enter to trigger click) if not properly guarded, causing an accessibility issue for keyboard users trying to interact with UI buttons.
**Action:** When adding global keyboard shortcuts, always check if the `document.activeElement` is an interactive element like a `BUTTON` or `INPUT` and return early to allow native keyboard interactions to function normally.
