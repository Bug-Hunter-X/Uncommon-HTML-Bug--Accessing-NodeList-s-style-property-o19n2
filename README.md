# Uncommon HTML Bug: Accessing NodeList's style property

This repository demonstrates a subtle bug that can occur when working with NodeLists in HTML and JavaScript.  The bug arises from incorrectly attempting to directly access the `style` property of a NodeList, which results in no changes being applied to the targeted elements.

## Bug Description
The bug lies in the JavaScript code that tries to change the color of all `div` elements to blue using `document.querySelectorAll('div').style.color = 'blue';`  NodeLists are collections of DOM elements, they don't have style property. To modify styles you must loop through each Node in the NodeList.

## Solution
The solution involves iterating through the NodeList obtained from `document.querySelectorAll` and setting the `style.color` property for each individual element.