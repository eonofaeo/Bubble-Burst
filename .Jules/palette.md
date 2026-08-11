
## 2026-08-09 - Ensure Buttons Have Keyboard Focus Outlines and Keyboard Shortcuts
**Learning:** Icon buttons and main action buttons lacked visible focus states (`:focus-visible`), making keyboard navigation difficult. Additionally, while ARIA labels were present, keyboard users or mouse users would benefit from knowing the specific keyboard shortcuts (like P for pause and M for mute) without having to guess or read the help text in the menu carefully.
**Action:** Add standardized `:focus-visible` styles to all interactive `.btn` and `.icon` classes, and include `title` attributes that expose the keyboard shortcuts on the relevant buttons.

## 2024-08-11 - Accessible Toggle Buttons and Dynamic Tooltips
**Learning:** For toggle buttons (like Mute/Unmute), it's important to use the `aria-pressed` attribute to indicate the state. However, when using `aria-pressed`, the W3C ARIA practices recommend keeping the `aria-label` static (e.g., always "Mute"). Modifying both the label and `aria-pressed` creates redundant screen reader announcements (e.g. "Unmute, toggle button, pressed"). Dynamic tooltips (`title` attribute) are fine.
**Action:** Use `aria-pressed` for toggle buttons to semantically indicate the state, keep the `aria-label` static, and dynamically update the `title` tooltip to provide clear, context-aware visual feedback.
