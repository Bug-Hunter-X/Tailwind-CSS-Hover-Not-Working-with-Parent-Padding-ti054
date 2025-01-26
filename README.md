# Tailwind CSS Hover Issue with Parent Padding

This repository demonstrates an uncommon bug in Tailwind CSS where hover effects on a button are unexpectedly overridden by the padding of its parent container.

## Bug Description

The button's hover styles (`hover:bg-blue-700`) are not applied when the parent div has padding (`p-4`).  This appears to be due to how Tailwind calculates the hover state's bounding box in relation to the padding.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Observe that the button's background color does not change on hover.

## Solution

The solution involves adding `relative` to the parent container's styles which ensures that the hover style properly applies to the button despite the parent's padding.