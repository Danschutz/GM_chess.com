# Grandmaster (GM) Simulation

This JavaScript script modifies the appearance of specific elements on a webpage to simulate a Grandmaster (GM) title. The changes are visual and temporary.

## What the Script Does

- Replaces specific links and `<div>` elements with a GM-styled appearance.

## How to Use

1. **Open the webpage** where you want to apply the script.
2. **Open Developer Tools** in your browser:
   - **Google Chrome / Microsoft Edge**: Press `Ctrl + Shift + I` (Windows/Linux) or `Cmd + Option + I` (Mac).
   - **Mozilla Firefox**: Press `Ctrl + Shift + K` (Windows/Linux) or `Cmd + Option + K` (Mac).
3. **Navigate to the "Console" tab**.
4. **Paste the JavaScript code** provided below and press `Enter`.

   ```javascript
   (function() {
       // Function to replace the first <a> element
       function replaceFirstAnchorElement() {
           var oldElement = document.querySelector('a[data-tooltip-target="6"][href*="badge-diamond"]');
           if (oldElement) {
               var newElement = document.createElement('a');
               newElement.className = 'user-chess-title-component';
               newElement.href = '/members/titled-players';
               newElement.target = '_blank';
               newElement.dataset.tooltipTarget = '12';
               newElement.textContent = 'GM';
               oldElement.parentNode.replaceChild(newElement, oldElement);
               console.log('First <a> element successfully replaced.');
           } else {
               console.log('First <a> element not found.');
           }
       }

       // Function to replace the second <a> element
       function replaceSecondAnchorElement() {
           var oldElement = document.querySelector('a[data-tooltip-target="6"][href*="web_play_live_arena"]');
           if (oldElement) {
               var newElement = document.createElement('a');
               newElement.className = 'user-chess-title-component';
               newElement.href = '/members/titled-players';
               newElement.target = '_blank';
               newElement.dataset.tooltipTarget = '12';
               newElement.textContent = 'GM';
               oldElement.parentNode.replaceChild(newElement, oldElement);
               console.log('Second <a> element successfully replaced.');
           } else {
               console.log('Second <a> element not found.');
           }
       }

       // Function to replace a <div> element
       function replaceDivElement() {
           var oldElement = document.querySelector('div[data-tooltip-target="0"]');
           if (oldElement) {
               var newElement = document.createElement('a');
               newElement.className = 'user-chess-title-component';
               newElement.href = '/members/titled-players';
               newElement.target = '_blank';
               newElement.dataset.tooltipTarget = '12';
               newElement.textContent = 'GM';
               oldElement.parentNode.replaceChild(newElement, oldElement);
               console.log('<div> element successfully replaced.');
           } else {
               console.log('<div> element not found.');
           }
       }

       // Execute the replacement of all elements
       replaceFirstAnchorElement();
       replaceSecondAnchorElement();
       replaceDivElement();
   })();