# Uncommon HTML Bug: Race Condition in DOM Manipulation

This repository demonstrates a subtle race condition that can occur in HTML when JavaScript code attempts to interact with the DOM (Document Object Model) before the elements have fully loaded.

## The Bug
The `bug.html` file contains a simple HTML page with a `div` element. A JavaScript script attempts to hide this `div` by setting its `display` style to `"none"`.  However, this happens before the browser has finished parsing and rendering the HTML, causing the script to fail silently.

## The Solution
The `bugSolution.html` demonstrates the correct approach. We use the `DOMContentLoaded` event listener to ensure the script only runs after the entire HTML document is parsed and the DOM is ready.

## How to reproduce the bug
1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe that the text inside the `div` remains visible because the JavaScript code fails to manipulate the element.

## How to fix the bug
1. Open `bugSolution.html` in a web browser.
2. Observe that the text inside the div is correctly hidden.  The `DOMContentLoaded` event listener ensures the script executes only after the DOM is fully constructed.

This example highlights the importance of proper DOM manipulation and asynchronous programming practices in web development.