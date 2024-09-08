# Grandmaster (GM) Simulation

![image](https://github.com/user-attachments/assets/bfd35922-206d-47b4-9fa6-7df2129f6bc0)


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

## Simple tutorial

![2024-09-08 11-28-32](https://github.com/user-attachments/assets/6109d910-f74b-4654-b444-17d80ff5eff9)

### Note..

- Important Note: To use this script and modify the appearance of the elements on the page, you need to be a Diamond Member. The visual change is temporary and only applies to your view of the current page.

![image](https://github.com/user-attachments/assets/9f32cd0d-45d7-4b22-a054-c7fc422e9904)



