---
title: "Using Developer Tools to Debug HTML and CSS: A Detailed Guide for Beginners"
date: "2025-03-20"
author: "Slavo"
image: "ts-big-o-notation.png"
excerpt: "Web development is an exciting field, but it also comes with challenges, especially when debugging and testing HTML and CSS."
isFeatured: false
category: "Type Script"
---

 Fortunately, modern web browsers like Google Chrome, Mozilla Firefox, Microsoft Edge, and Safari have built-in Developer Tools (DevTools), which are incredibly useful for inspecting, testing, and debugging web pages. If you're new to web development, understanding how to leverage these tools effectively can save you time and frustration as you refine your skills. This guide will take you through the process of using Developer Tools to debug HTML and CSS step by step. Whether you're troubleshooting layout issues, testing new styles, or optimizing your code, these tools are indispensable. By the end of this guide, you'll be well-equipped to identify problems and fix them quickly, ensuring that your web projects look and function the way you intended.
Developer Tools (DevTools) are essential sets of built-in utilities available in modern web browsers like Google Chrome, Firefox, Safari, and Microsoft Edge. These tools allow developers to inspect, debug, and optimize websites by providing insights into various elements like HTML structure, CSS styles, JavaScript behavior, network activity, and more. They are indispensable for creating efficient, responsive, and bug-free web applications.
Key Features and Functions of Developer Tools:
Inspecting HTML & DOM:
 DevTools allow developers to view and inspect a web page's Document Object Model (DOM), a hierarchical representation of its page. In real-time, developers can view and manipulate individual elements like paragraphs, headings, images, links, etc. real-time. This is invaluable for troubleshooting layout issues, verifying the presence of elements, or testing modifications.
CSS Manipulation & Styling:
 The Elements panel in DevTools displays the HTML structure and associated CSS rules. Without updating the source files, developers can instantly modify CSS properties, such as colors, margins, padding, font sizes, and more. This makes experimenting with different styles and seeing the changes live easy.
JavaScript Debugging:
 DevTools include an integrated JavaScript debugger that allows developers to set breakpoints, inspect variables, step through code, and evaluate expressions. This is crucial for identifying and fixing issues in client-side scripting. JavaScript code can also be executed directly from the console, allowing for quick testing of snippets or interacting with the page programmatically.
Network Monitoring:
 DevTools provides a network panel that allows developers to track all network requests (like API calls, images, scripts, etc.) made by a web page. This feature is essential for performance optimization, as it shows the loading times of various resources and helps identify bottlenecks or failed requests. You can also see the response status, request headers, and response body, which is helpful for debugging issues with server communication.
Performance Analysis:
 The Performance panel lets developers record and analyze page load times, script execution, and other resource usage. It provides detailed insights into how the browser renders the page, where bottlenecks occur, and which resources take the longest to load. Optimizing page performance often involves identifying slow JavaScript execution, large image files, or inefficient CSS rendering.
Responsive Design Testing:
 DevTools comes with a device simulation feature, allowing developers to test how their websites look and behave on different screen sizes and resolutions. This is especially useful for ensuring that websites are mobile-responsive and function well across a variety of devices, such as smartphones, tablets, and desktop computers.
Console & Logging:
 The Console panel logs messages, errors, and warnings from JavaScript running on the page. Developers can also use it to execute JavaScript directly, which helps test small pieces of code or inspect objects. Console messages are an invaluable debugging tool, providing insight into code execution and potential problems.
Security & Accessibility Audits:
 DevTools often include features for auditing a website's security and accessibility. For example, the Lighthouse tool can run audits to check for everyday web performance, SEO, and accessibility best practices. It generates a detailed report that developers can use to improve their website's overall quality and user experience.
Source Control and Versioning:
 Many browsers, such as DevTools, integrate with version control systems like Git, making it easier for developers to track changes to the codebase, review commits, and handle source code directly from within the browser.
How DevTools Enhance the Development Process:
Instant Feedback: Changes made in DevTools are reflected immediately, enabling developers to see the results without refreshing the page or altering the underlying code files.
Real-Time Debugging: DevTools provides an efficient environment where developers can inspect and modify running web applications in real-time. This accelerates the process of finding and fixing bugs.
Efficient Troubleshooting: Whether it's an issue with the layout, scripts, or network requests, DevTools help identify precisely where things are going wrong. This makes it faster and easier to fix problems.
Enhanced Performance: By monitoring performance metrics and understanding how resources are loaded, developers can optimize their websites to load faster, improve responsiveness, and reduce overall resource consumption.
Accessing Developer Tools (DevTools)
DevTools is a powerful suite of tools provided by modern web browsers that allow developers to inspect and debug web pages directly from the browser. It's essential for tasks like inspecting HTML structure, testing JavaScript code, and modifying CSS styles in real time.
Let's review how to access Developer Tools in the most popular browsers.
Google Chrome
Google Chrome offers an intuitive way to access DevTools:
Right-click on any page element: To inspect a webpage element (e.g., text, image, or button), right-click on it and select Inspect. This will open the DevTools panel and highlight the corresponding HTML element in the Elements tab.
Keyboard Shortcut: You can use the following shortcuts to open DevTools:
Windows/Linux: Press Ctrl + Shift + I.
macOS: Press Cmd + Option + I.
Once opened, the DevTools panel in Chrome will appear at the bottom or side of your browser window and provide a set of tabs, such as Elements, Console, Network, Performance, etc.
Mozilla Firefox
In Mozilla Firefox, the steps are very similar to Chrome, with the following options:
Right-click on any page element: Right-click on a component on the page and select Inspect Element. This will open the DevTools and highlight the element in the Inspector tab.
Keyboard Shortcut: You can also open DevTools using the following keyboard shortcuts:
Windows/Linux: Press Ctrl + Shift + I.
macOS: Press Cmd + Option + I.
Once opened, Firefox's DevTools interface is almost identical to Chrome's, with tabs for Inspector, Console, Debugger, Network, and Performance.
Microsoft Edge
Edge uses the same Chromium engine as Chrome, so the process for accessing DevTools is very similar:
Right-click on any page element: Right-click anywhere on the page and choose Inspect from the context menu. This opens the DevTools panel.
Keyboard Shortcut: Use the following shortcuts:
Windows: Press Ctrl + Shift + I.
macOS: Press Cmd + Option + I.
Microsoft Edge's DevTools has a layout almost identical to Google Chrome's, making it easy for developers to transition between browsers. The main sections include the Elements, Console, Network, and Sources tabs.
Safari (macOS Only)
Safari requires a small setup step to access DevTools, as the tools are hidden by default:
Enable the Develop menu:
Open Safari Preferences by going to the Safari menu at the top-left corner of the screen and selecting Preferences.
Go to the Advanced tab and check the Show Develop menu box in the menu bar.
Right-click on a page element: After enabling the Develop menu, right-click on any element and choose Inspect Element. This will open the DevTools panel.
Keyboard Shortcut: You can also use the shortcut:
macOS: Press Cmd + Option + I.
Once enabled, Safari's DevTools will open in a panel that allows you to inspect HTML elements, edit CSS, and debug JavaScript. The layout and tools are similar to those found in Chrome and Firefox.
Overview of Key Sections in DevTools
You'll be presented with several panels once you've opened DevTools in your browser. These panels provide different functionalities for web development and debugging:
Elements (or Inspector): This panel shows the webpage's HTML structure. It lets you inspect and edit the HTML and CSS directly in the browser. You can modify the page's structure and styles in real time, particularly useful for debugging layout issues.
You can see the entire page's DOM (Document Object Model), click on elements to inspect them, and change their properties.
The Styles section (usually on the right side) shows the CSS rules applied to the selected element. You can also add or modify CSS properties directly in this section.
Console: The Console is where JavaScript output (logs, errors, etc.) appears. It's beneficial for debugging JavaScript, testing snippets of code, and viewing any errors or warnings generated by the page's scripts.
Network: The Network tab shows all network requests the page makes, such as HTTP requests for images, scripts, and stylesheets. This is useful for monitoring page load performance and debugging network issues.
Performance: This tab helps with performance profiling, such as analyzing page load times and identifying performance bottlenecks in the page's scripts or rendering.
Sources: The Sources tab allows you to view and debug the JavaScript source code used by the webpage. You can set breakpoints and step through the code line by line to diagnose issues.
Application: This tab allows you to inspect web app resources such as cookies, local storage, session storage, and more.
Security: This section provides information about the page's security, including SSL/TLS certificate details and any security issues, such as mixed content warnings.
The Elements Panel: Inspecting and Modifying HTML
The Elements panel is a core feature in web development tools that browsers like Google Chrome, Firefox, and others provide. It's an essential tool for inspecting and modifying the HTML structure of a webpage in real time. It allows you to interact with the Document Object Model (DOM), which represents the page's HTML elements. The Elements panel is invaluable for debugging, optimizing, and making on-the-fly adjustments to a webpage. Below, we will dive into a detailed explanation of how this tool can be used to inspect and modify your web page's HTML.
What the Elements Panel Allows You to Do:
Inspect Individual Elements: You can view detailed information about any element on the page, including its HTML tag, attributes, and content.
Modify the HTML in Real-Time: The Elements panel allows you to make live changes to the HTML code and see the results immediately on the page. This is useful for testing changes before implementing them permanently.
View the Structure of the DOM: The panel displays the DOM as a hierarchical tree, making it easy to see how elements are nested within one another.
Analyze Relationships Between Elements: You can examine how elements are positioned about one another and investigate any parent-child relationships (e.g., a < div> containing a < p> or < img>).
Find and Fix Errors in Your HTML: The Elements panel helps spot potential issues in the HTML structure, such as missing tags, unclosed tags, and improper nesting. This can be crucial for troubleshooting layout, rendering, or functionality issues on the page.
Navigating the DOM Tree:
When you open the Elements panel, the page's structure is shown as a DOM tree. This tree is a visual representation of how elements are nested within each other. Each node in the tree represents an HTML tag or an element. Let's break down how to navigate this structure:
Top-Level Tags: At the root of the DOM tree, you'll typically find tags like < html>, < head>, and < body>. These serve as the container elements for the rest of the page's content. The < html> tag encompasses everything on the page, while the < head> contains metadata like the title, links to stylesheets, and scripts, and the < body> contains the visible content.
Child Elements: Elements within the < body> tag are the next level of nesting in the DOM tree. For example, you might see a < div>, < header>, or < footer>. These elements can have further nested elements inside them, such as paragraphs (< p>), headings (< h1>, < h2>), images (< img>), or even other < div> tags.
Attributes: Next to each HTML tag, you'll see attributes that provide additional information about an element. Common attributes include:
Id: A unique identifier for an element.
Class: A class name that can be used for styling or JavaScript manipulation.
Src: Specifies the source of an image or video.
Alt: Provides alternative text for images, improving accessibility.
Attributes are essential for styling with CSS or interacting with elements using JavaScript.
Element Content: Text and other content within tags (e.g., the text inside a < p> tag or an image's alt attribute) are also displayed. The text appears directly beneath the element tag in the DOM tree, often indented to show its relationship with the parent tag.
Nestable Tags: As you dig deeper into the tree, you will see more nested elements. For example, a < ul> (unordered list) tag might contain < li> (list items) tags. Similarly, a < div> can hold any number of child elements, such as < p>, < a>, < img>, and others.
How to Inspect and Modify HTML:
The Elements panel offers interactive features for inspecting and modifying HTML. Here's a step-by-step guide on how to use it effectively:
Inspect Elements:
Right-click on any part of the webpage and select "Inspect" or "Inspect Element" (depending on your browser).
This will highlight the corresponding element in the DOM tree in the Elements panel.
You can click through various parts of the DOM tree to inspect different elements.
Modify HTML:
To edit an element's HTML, right-click the element in the Elements panel and choose Edit as HTML.
You can now modify the content and attributes or even add new elements.
Any changes you make are immediately reflected on the webpage, allowing you to see the effect of your edits in real time.
Modify Attributes:
You can click on an element's attributes in the Elements panel to edit them. For example, you can change the src attribute of a < img> tag to update the image being displayed or modify the href attribute of a link.
Delete or Add Elements:
Right-click an element in the DOM tree and select Delete Element to remove it from the page (temporarily).
To add an element, right-click an existing element and then use the Edit HTML option to insert a new component before or after it.
Check for Errors:
Look for any visual indicators in the panel, such as highlighted tags or red underlines, which may indicate errors in your HTML structure.
The browser will sometimes warn you about unclosed tags or invalid attributes.
The Advantages of Using the Elements Panel:
Immediate Feedback: You can test code changes without reloading the page or modifying files in your text editor, speeding up your workflow.
Debugging: The Elements panel helps diagnose layout issues or find unclosed tags, misplaced elements, or improperly structured HTML that may affect the page's rendering.
Live Editing: Making real-time changes gives you the flexibility to experiment with different HTML structures and test how they affect your page's visual presentation before implementing permanent changes.
Learning Tool: The Elements panel provides a way to learn how different HTML elements are structured and related to one another, offering insight into web development.
Inspecting an Element
To inspect a specific element on your web page, use the Inspect tool in your browser's Developer Tools. This feature is invaluable for debugging and analyzing the structure and styles of your website. Here's a more detailed explanation of how it works:
Right-click and Inspect:
 To inspect an element, right-click on any element you want to investigate and select Inspect or Inspect Element from the context menu. This will open the Developer Tools window, typically at the bottom or side of the screen.
Elements Panel:
 Once you open the Inspector, the Elements panel is automatically activated. This panel represents your page's Document Object Model (DOM) tree. The DOM is a hierarchical structure that represents the HTML elements and their relationships to each other.
Highlighting in DOM Tree:
 The element you right-clicked on will be highlighted in the DOM tree, which corresponds to the HTML structure. This is useful for understanding the parent-child relationships between components. You can expand and collapse these elements to dive deeper into nested structures like lists, tables, and forms.
Viewing HTML Code:
 The selected element's HTML code will appear in the Elements panel. You can see the element's tag, such as < div>, < p>, or < a>, and all its attributes (e.g., class, id, style, etc.). This allows you to examine the element's markup and understand its structure.
Modifying HTML in Real-Time
One of the most powerful features of the browser's developer tools is the ability to modify HTML directly in the Elements panel and see changes in real time. This is useful for testing content changes without editing files and reloading the page. Here's how to do it:
Edit Text:
 To edit text within an element, double-click on the text content inside tags like < p>, < h1>, or < span>. After double-clicking, you can type new text, and the page will immediately update to reflect the changes. This is useful for quick text content edits.
Change Element Attributes:
 You can also modify the attributes of HTML elements. For example, if you want to change the source of an image, find the src attribute inside the < img> tag and edit the URL. Similarly, you can edit href in anchor (< a>) tags or other attributes such as alt, title, etc.
Delete Elements:
 Right-click on an element in the Elements panel and choose Delete Element. This will remove the selected element from the page. Remember that this change is temporary and only affects the current session. Once you refresh the page, the changes will be lost unless the HTML code is modified in the source files.
Adding New HTML Elements
You can also add new HTML elements directly through the Developer Tools:
Edit as HTML:
 Right-click on a parent element (such as a < div>) and choose Edit as HTML. This will open the element's HTML in an editable format in the Elements panel.
Insert New Tags:
 In the edit mode, you can insert new HTML tags, such as < p>, < h2>, < ul>, or even custom tags. After you add the new elements, click outside the editor, and the changes will appear instantly on the page.
The Styles Panel: Debugging and Modifying CSS
The Styles panel is an essential tool for debugging and modifying the CSS of your page. It allows you to see which CSS rules are applied to an element and will enable you to change them instantly. Here's a breakdown of how the Styles panel works:
Viewing Applied Styles:
 When you select an HTML element in the Elements panel, the Styles panel shows all the CSS rules applied to that element. These rules come from various sources, such as:
Inline styles: CSS is applied directly within the style attribute of an HTML tag.
Internal styles: CSS defined within < style> tags in the < head> section of the page.
External styles: CSS from linked external stylesheets, usually defined in a .css file.
The panel lists these rules in order of specificity, with the most specific rule appearing at the top. If a rule is overridden by a more specific one, it will be crossed out.
Rule Origin:
 Each rule will display where it comes from. It could be from an inline style, an internal < style> tag, or an external stylesheet. This helps you identify the source of the rule and make informed decisions when debugging.
Overridden Styles:
 If a CSS rule is overridden by a more specific rule (like a class selector overriding an element selector), it will be crossed out in the Styles panel. This makes it easy to see which styles are no longer applied to the element.
Modifying CSS Live
The Styles panel allows for live CSS editing, which is great for testing different styles on the fly without needing to edit your CSS files and reload the page. Here's how you can modify the CSS:
Change CSS Values:
 Click on any CSS property value (e.g., color: red or padding: 10px;). A text box will appear, and you can type in a new value. The page will instantly reflect the changes, making it easy to test different values without reloading.
Toggle CSS Properties:
 You can turn CSS properties on or off by clicking the checkbox next to each property in the Styles panel. This is useful for testing how a page looks with or without specific styles applied. For example, you can toggle display none or visibility hidden to see how an element behaves when it's hidden.
Add New CSS Rules:
 At the bottom of the Styles panel is a button to add a new rule. This allows you to add custom styles to the selected element. You can input new properties and values and see how they affect the page instantly.
Debugging CSS Layout and Box Model
One of the foundational concepts in CSS is the Box Model, which governs the sizing and positioning of elements on a web page. The Box Model is crucial because it determines an element's space, including the content, padding, borders, and margins.
Here's a breakdown of the Box Model:
Content: This is the actual content of the element, such as text, images, or any media. It's the innermost part of the box, which is directly affected by the width and height properties.
Padding: Padding is the space between the content and the element's border. It affects the element's size by pushing the border away from the content. The padding can be set individually for each side (top, right, bottom, left) or in shorthand (e.g., padding: 10px).
Border: The border surrounds the element and comes after padding. It can have a specific width, color, and style (solid, dashed, dotted, etc.). Like padding, the border adds to the total size of the element.
Margin: The margin is the outermost space around an element. It separates it from other elements on the page and is the most flexible space. Margins can collapse if two adjacent elements have margins on opposite sides.
Why is the Box Model Important?
The Box Model affects how an element interacts with others regarding positioning, spacing, and overall layout. For example, if you have an element with a fixed width and height, adding padding or borders will increase the total space the element occupies unless the box-sizing border-box property is used.
By inspecting the Box Model in the browser's Developer Tools (DevTools), you can visualize how much space is being taken up by each part of the element. This helps in troubleshooting layout issues such as:
Overlapping elements: If elements are overlapping, it might be due to unaccounted-for padding, borders, or margins.
Misaligned elements: Padding and margins can shift elements unintentionally, causing misalignment.
Elements being too large: If a component appears larger than intended, check the Box Model to ensure the padding and borders aren't adding unexpected size.
CSS Grid and Flexbox Debugging
CSS Grid and Flexbox are robust layout systems that allow flexible, responsive designs. However, debugging them can be tricky sometimes, especially if elements don't align or behave as expected. Here's how DevTools can help in debugging these layouts:
CSS Grid Debugging
CSS Grid enables complex layouts with rows and columns; it can be challenging to visualize how elements are placed within the grid. DevTools offers a Grid Overlay that makes it easier to debug grid layouts. Here's how it works:
Grid Lines and Cells: The Grid Overlay displays the grid lines, making it clear where the rows and columns are. This helps to identify whether the grid items are correctly placed in the intended grid cells.
Item Positioning: It shows how each grid item spans across rows and columns. You can quickly identify issues with items not spanning or aligning correctly.
Common Grid Issues:
Grid items overlap if they are placed outside the grid's defined areas.
Elements may not align as expected due to incorrect grid-template definitions or missing properties like grid-column or grid-row.
Flexbox Debugging
Flexbox is another layout system that provides flexibility in how items are distributed along a container's axis. Sometimes, Flexbox can lead to unexpected results due to misused properties or misunderstanding of its behavior. DevTools provides a Flexbox Overlay that makes it easier to troubleshoot Flexbox layouts.
Flex Container and Items: The Flexbox Overlay highlights the flex container and its items, showing how space is distributed between them. This helps visualize how justify-content, align-items, and align-self properties affect the layout.
Item Alignment: It helps you spot alignment issues, such as items that are not centered or stretched as expected.
Common Flexbox Issues:
Items may not be distributed evenly if justify-content or align-items properties are incorrectly set.
Items may not resize as expected due to improper use of flex-grow, flex-shrink, or flex-basis.
Live Testing with Device Toolbar
As a web developer, it is critical to ensure your web pages are responsive and look great across various devices. The Device Toolbar in DevTools simulates different screen sizes and resolutions, making it easy to test how your webpage appears on mobile, tablet, and desktop devices.
Enabling the Device Toolbar:
Open DevTools: Open the Developer Tools in your browser (usually by pressing F12 or Ctrl + Shift + I).
Toggle Device Toolbar: Click on the Toggle Device Toolbar icon, which looks like a small tablet and phone.
Select a Device: From the dropdown menu, choose a device to simulate, such as an iPhone, iPad, or Android phone. Alternatively, you can manually adjust the width and height of the viewport to test custom screen sizes.
Why Test on Different Devices?
Mobile-friendliness: Testing on smaller devices ensures your site is optimized for mobile users, with proper touch controls and scaling.
Responsive Design: By adjusting the screen size, you can verify if the layout adapts and reflows correctly across different screen resolutions.
Viewport-specific issues: It allows you to identify issues such as content being cut off, improper scaling, or incorrect element visibility on smaller screens.
Debugging CSS Animations
CSS animations can sometimes be tricky to debug because they involve timing and transitions that might not be immediately apparent. DevTools offers an Animations Panel that simplifies the process of debugging CSS animations.
Timeline View: The Animations panel shows a timeline of the animation so you can see exactly how the animation progresses over time.
Pause and Play: You can pause and play the animation at any point to better understand how it behaves and spot any discrepancies in timing, delays, or other issues.
Animation Speed: You can slow down the animation in DevTools to examine each frame closely, which is especially helpful for complex animations.
Common Animation Issues:
Timing issues: Animations might not start or finish as expected due to incorrect timing functions or delays.
Overlapping animations: If multiple animations run simultaneously, they might interfere, causing unexpected results.
Choppy animations: If animations feel laggy, it could be due to performance issues such as heavy reflows or lack of hardware acceleration.

Happy coding!

\*\* Book Recommendation:

- [React and React Native: A complete hands-on guide to modern web and mobile development with React.js, 3rd Edition](https://amzn.to/3CStF7m)
- [React Key Concepts](https://amzn.to/43XOCJM)
- [Pragmatic Programmer](https://amzn.to/3W1P4oL) **_The: Your journey to mastery, 20th Anniversary Edition_**

[Mentorship & Consulting - Contact us for more info](/contact)

**_Join Our Discord Community_** [Unleash your potential, join a vibrant community of like-minded learners, and let's shape the future of programming together. Click here to join us on Discord.](https://discord.gg/A75tvDvZ)

**_For Consulting and Mentorship, feel free to contact_** [slavo.io](/contact)
