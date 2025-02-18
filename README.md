# Inconsistent Styling with :nth-child(2n) Selector on Large Lists

This repository demonstrates a subtle bug related to the CSS `:nth-child(2n)` selector when applied to very large lists. The selector, intended to style every other list item, inconsistently stops applying the style after a certain number of items.  This occurs in some browsers and is likely due to performance optimizations.

## Bug Description
The provided CSS uses `:nth-child(2n)` to style even-numbered list items. While functional on smaller lists, it produces inconsistent results when used with hundreds or thousands of list items. The styling unexpectedly stops applying at an unpredictable point.

## Reproduction
1. Clone this repository.
2. Open `bug.html` (or similar file, if created) in a web browser.
3. Observe the inconsistent styling applied to the list items.  The behavior might vary slightly depending on the browser and the number of items.

## Solution
The solution involves either employing a different approach (e.g., JavaScript-based styling) or a more efficient and reliable selector (as shown in `bugSolution.css`).

## Note
This bug highlights potential performance considerations when working with complex CSS selectors and large lists. The behavior isn't a standard CSS specification error, but rather a consequence of browser-specific implementation details and optimizations.