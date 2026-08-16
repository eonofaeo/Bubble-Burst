
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.
## 2026-08-16 - Hidden Elements Accessibility
**Learning:** Using `opacity: 0` visually hides an element but leaves it in the DOM where screen readers and keyboard navigation (tabbing) can still focus it, causing phantom tab stops.
**Action:** Always pair `opacity: 0` with `visibility: hidden` (or `display: none`) to fully remove the element from the accessibility tree.
