# CSS `calc()` Function Issues

This repository demonstrates an uncommon error involving the CSS `calc()` function.  The `calc()` function is powerful for dynamic calculations, but it can lead to problems when used with percentage values and dynamic parent widths.

## Bug
The `bug.css` file contains CSS code that attempts to set the width of an element using `calc(50% - 10px)`.  This works well if the parent element has a sufficiently large width. However, if the parent is too small, it results in a negative width, causing unexpected behavior.

Additionally, percentage calculations within `calc()` can be problematic if the parent's size is dependent on other dynamic elements that aren't yet fully rendered.

## Solution
The `bugSolution.css` file provides several solutions to this issue, including the use of `min()` and `max()` functions within `calc()` to prevent negative widths. It also includes best practices for using `calc()` to make sure the calculations are correct and accurate.