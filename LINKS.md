

[QUARTZ](https://quartz.jzhao.xyz/build)

[Github Daxuefayu](https://github.com/A000045/daxuefayu/tree/v4/content/%E5%A4%A7%E5%AD%A6%E6%B3%95%E8%AF%AD)

[nicolevanderhoeven documentation](https://notes.nicolevanderhoeven.com/How+to+publish+Obsidian+notes+with+Quartz+on+GitHub+Pages)

[Youtube](https://www.youtube.com/watch?v=6s6DT1yN4dw)


## Quartz Git Issues

[Explorer Component Hidden On Mobile View #1006](https://github.com/jackyzha0/quartz/issues/1006)
	<span style="background:#d4b106">-</span> [Responsive design for all high DPI displays #455](https://github.com/jackyzha0/quartz/issues/455)

### Archived
[My Comment on the forum](https://github.com/jackyzha0/quartz/issues/769)


## GPT Suggestion

### Confirming Desktop-Only CSS

1. **Inspect CSS Rules**:
    
    - Open Chrome Developer Tools (`Ctrl+Shift+I` or right-click > "Inspect").
    - Navigate to the "Elements" tab and select the `<div class="explorer desktop-only">`.
    - In the "Styles" pane on the right, look for CSS rules that apply to `.desktop-only`. You might find something like `display: none;` or similar styles that hide the element on mobile screens.
2. **Check Media Queries**:
    
    - Still in the Developer Tools, look for any media queries in the CSS that might be hiding elements with the `desktop-only` class on smaller screens. Media queries might look something like:

`@media (max-width: 768px) {`
  `.desktop-only {`
    `display: none;`
  `}`
`}`

3. - If such a rule exists, it confirms that the `desktop-only` class is used to hide the element on mobile devices.

### Resolving the Issue

1. **Override CSS Temporarily**:
    
    - In the Developer Tools, you can temporarily override the CSS to test visibility. In the "Styles" pane, uncheck or modify rules that hide the `desktop-only` class. For instance, you might change `display: none;` to `display: block;`.
2. **Adjust CSS**:
    
    - If you have access to the CSS files, locate the relevant styles and adjust them. You might want to modify or remove the media queries that hide the `.desktop-only` class or add a condition that ensures it's visible on your desktop setup.

`@media (max-width: 768px) {`
  `.desktop-only {`
    `display: block !important; /* or adjust as needed */`
  `}`
`}`

3. **Check Responsive Design Settings**:
    
    - Make sure your responsive design settings are correctly configured in your hosting setup. Sometimes, configurations or JavaScript can dynamically adjust the display based on screen size.
4. **Test Different Devices**:
    
    - To ensure the changes work, test your webpage on different screen sizes. You can use the Developer Tools to simulate various devices and viewports.

By examining and adjusting the CSS rules related to the `desktop-only` class, you should be able to determine if this is the cause of the missing Explorer panel and make it visible as needed.