# CSS Bug: Unexpected Behavior with Pseudo-Classes, Sibling Combinators, and Dynamic Classes

This repository demonstrates an uncommon CSS bug related to the interaction between pseudo-class selectors, sibling combinators, and dynamically applied classes using JavaScript.  The bug manifests when a pseudo-class selector (like `:hover`) is used on an element that is selected using a sibling combinator and the target element's class is added or removed after page load.

## Bug Description

The expected behavior is that when the element with the sibling combinator and pseudo-class is hovered, the affected element will reflect the style change specified in the CSS.  However, this may not work correctly if the affected element's class changes dynamically after page load, leading to unexpected styling results. This is because the browser may not correctly recalculate the CSS selectors due to the change in class after the CSS is initially evaluated. 

## Steps to Reproduce

1. Clone this repository.
2. Open `index.html` in your browser.
3. Observe the inconsistent styling of the elements upon hovering and toggling the button which will add/remove a class. 

## Solution

The solution involves optimizing the CSS selector to be robust and handle the dynamic changes better. Often this can be solved by using more specific selectors, or avoiding the use of sibling combinators altogether in cases with dynamic changes.

Refer to the file `solution.css` for an example of a solution.