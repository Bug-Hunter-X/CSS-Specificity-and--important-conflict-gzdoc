# CSS Specificity and !important Conflict

This repository demonstrates a subtle bug related to CSS specificity and the `!important` declaration.  The bug showcases how the order of style declarations and the use of `!important` can interact unexpectedly when dealing with multiple class selectors and inheritance.

## Bug Description

The bug lies in the unexpected behavior of font size inheritance when using `!important` along with class selectors that overlap. A higher-specificity rule with `!important` is overridden by a lower-specificity rule later in the stylesheet, which violates the expected behavior regarding `!important`'s precedence.  This is particularly challenging to debug as it relies on the specific order and combination of classes.

## Reproduction

1. Clone this repository.
2. Open `bug.css` to see the problematic CSS code.
3. Create an HTML file to test the CSS (example provided in `index.html`).
4. Observe the rendered font size.  It will not match the expected size based on normal CSS specificity rules.

## Solution

The solution is detailed in `bugSolution.css`. It addresses the problem by restructuring the CSS rules to ensure the intended font size is consistently applied. This highlights the importance of carefully managing CSS specificity and avoiding reliance on `!important` whenever possible.