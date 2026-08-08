## 2026-08-08 - Keyboard Accessibility with Opacity
**Learning:** Hiding elements using `opacity: 0` and `pointer-events: none` does not remove them from the keyboard tab order. This can trap keyboard focus on invisible elements, causing severe confusion for screen reader and keyboard users.
**Action:** Always use `visibility: hidden` (or `display: none`) in conjunction with opacity when removing elements from the screen to ensure they are also removed from the focus order. Transitioning `visibility` allows for smooth fade-outs without breaking accessibility.
