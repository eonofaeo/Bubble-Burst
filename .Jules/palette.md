
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.

## 2026-10-24 - Handle Screen Reader Accessibility for Repeating Visual Elements
**Learning:** For dynamic elements like the visual "hearts" indicating remaining lives, appending a single repetitive character multiple times (e.g. ♥♥) is confusing for screen readers, which will simply read out the repeated characters. Using `aria-pressed` to indicate toggle states like Mute is much clearer than just relying on changing icons, as users might not understand that the icon represents a toggle button for state.
**Action:** Always wrap repeating visual elements indicating quantity in an accessible container with `role="status"` and a clear, descriptive `aria-label` (e.g. "Lives: 3"). The individual repeating decorative characters should be hidden from assistive technology using `aria-hidden="true"`. Use `aria-pressed` and dynamic text labels for toggles.
