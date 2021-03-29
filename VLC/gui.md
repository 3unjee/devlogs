# VLC 4 - GUI improvements proposal / WIP

This document is a list of *potential* improvements for the upcoming release of VLC 
(4.0 and beyond). It focusses on the desktop Windows / Linux version. It should be updated along 
the way when something is added or completed.

## UX
- Improve page transitions and animations (when clicking on different tabs).
    - Make sure we can disable or configure them from a single place.
- Improve buttons and tab buttons animations / behavior to make them instant.
- Improve scrolling area(s) performance, they are too slow for some reason.
- Make a stacked "error popup" implementation instead of a list.

## UI
- Improve buttons area (by reducing margins) and highlight to make them more subtle
(i.e. as defined in the original design).
    - When hovering we could make a thicker border or display a soft shadow.
- Improve the scrollbar visiblity and make them closer to the native look
(both on Windows and Linux).
- Improve shadows under navigation tabs to make them closer to the original design.
- Increase grid and list delegate(s) margins to make them clearer and flat
(to be confirmed, can be subjective).
    - This allows us to avoid shadowing all over the place (a remnant of the skeuomorphic era).
- Use real icons (svg) instead of font icons.
    - This allows us to have colored and animated icons.
    - This allows us to have lazy loading on icons (faster GUI startup).
    - Font icons are web practices and we are genuine hairy developers (OK I'm trolling a bit).
- Make "error popups" look better. They are currently list based and not optimal for readability.

## Got anything in mind ?

Tell me here -> bunjee@omega.gg

## Author

Benjamin Arnaud aka [bunjee](http://bunjee.me) | <bunjee@omega.gg>
