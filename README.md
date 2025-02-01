# Uncommon HTML Error: DOM Element Access Before Page Load

This repository demonstrates a common yet often overlooked HTML error: attempting to access a DOM element before the browser has fully parsed and rendered the HTML. This issue usually manifests as unexpected `null` or `undefined` errors in JavaScript code, leading to application malfunctions.

## The Bug

The `bug.html` file contains a simple HTML structure with a `div` element and a script. The script tries to log the `innerText` of the `div` element before the page is fully loaded. This commonly happens when scripts are placed in the `<head>` section.

## The Solution

The `bugSolution.html` file presents the corrected version. Instead of accessing the element directly, it uses the `DOMContentLoaded` event.  This ensures that the script executes only after the entire HTML document has been parsed, preventing the `null` or `undefined` errors.