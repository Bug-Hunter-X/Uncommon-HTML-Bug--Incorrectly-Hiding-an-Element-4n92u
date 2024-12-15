# Uncommon HTML Bug: Incorrectly Hiding an Element

This repository demonstrates a common yet subtle bug in HTML involving incorrect element hiding.  The issue arises from attempting to manipulate an element's style property before the element is fully parsed into the Document Object Model (DOM).  The solution showcases how to correctly handle this using event listeners.

## Bug Description
The provided `bug.html` file attempts to hide a div element using inline styling and JavaScript.  However, this approach will not work consistently because the JavaScript executes before the element is fully rendered in the DOM.  This can lead to unexpected behavior and the element remaining visible.

## Solution
The `bugSolution.html` file demonstrates the correct approach.  Instead of directly manipulating the style, we use the `DOMContentLoaded` event listener to ensure the JavaScript executes only after the entire DOM is ready. This guarantees that the element exists and can be successfully manipulated.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser. Note that the element might not be hidden.
3. Open `bugSolution.html` in a web browser.  The element will be correctly hidden.

## Conclusion
This example highlights the importance of understanding the DOM's lifecycle when manipulating elements using JavaScript. Always ensure your scripts execute after the DOM is ready to avoid this type of error.