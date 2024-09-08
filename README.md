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

# My Repository

This repository contains a JavaScript script for updating HTML elements on a web page.

## JavaScript Code

Below is the JavaScript code used to replace specific HTML elements:

```javascript
const selectors = [
    'a.mvp-badge-component.mvp-badge-diamond.mvp-badge-link[href*="web_play_live_arena"]',
    'a.mvp-badge-component.mvp-badge-diamond.mvp-badge-link[href*="web_play"]',
    'div.cc-user-badge-component.cc-user-badge-diamond'
];

const newHTML = '<a class="user-chess-title-component" href="/members/titled-players" target="_blank" data-tooltip-target="1">GM</a>';

selectors.forEach(selector => {
    const elements = document.querySelectorAll(selector);

    if (elements.length > 0) {
        elements.forEach(element => {
            element.outerHTML = newHTML;
        });
    } else {
        console.log(`No elements found for the selector "${selector}".`);
    }
});
 ```



## Simple tutorial

![2024-09-08 11-28-32](https://github.com/user-attachments/assets/6109d910-f74b-4654-b444-17d80ff5eff9)

### Note..

- Important Note: To use this script and modify the appearance of the elements on the page, you need to be a Diamond Member. The visual change is temporary and only applies to your view of the current page.

![image](https://github.com/user-attachments/assets/0ff24dd1-dd08-4853-8411-22c59e75f203)

### Note plus

- as I gave up on the project it still has some flaws like you get rating not update, but don't worry it's just visual

![image](https://github.com/user-attachments/assets/af1604f8-ab98-4294-993b-5e10696f34d6)




