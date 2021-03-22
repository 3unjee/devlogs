# GUI improvements proposal for VLC 4

## UX
- Improve transition animations betwen pages (when clicking on the different tabs).
    - Make sure we can disable or configure them from a single place.
- Improve buttons and tab buttons animations and behavior to make them instant.
- Improve scrolling area(s) performance, they are too slow for some reason.

## UI
- Improve buttons area (by reducing margins) and highlight to make them more subtle (i.e. as defined in the original design)
- Improve the scrollbar visiblity and make them closer to the native look (both on Windows and Linux).
- Improve shadows under navigations tabs to make them closer to the original design.
- Increase grid and list delegate margins to make them clearer and flat (can be subjective, to be confirmed).
    - This allows us to avoid shadowing all over the place (a remnant of the skeuomorphic era).
- Use real icons (svg FTW) instead of font icons.
    - This allows us to have colored and animated icons.
    - This allows us to have lazy loading on icons (faster GUI startup).
    - Font icons are web practices and we are genuine developers (OK I'm trolling a little bit).
