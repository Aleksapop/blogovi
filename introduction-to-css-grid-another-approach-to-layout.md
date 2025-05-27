---
title: "Introduction to CSS Grid: Another Approach to Layout"
date: "2025-03-20"
author: "Slavo"
image: "ts-big-o-notation.png"
excerpt: "When creating complex layouts for web design, CSS has evolved to offer several powerful tools that make it easier and more flexible than ever."
isFeatured: false
category: "Type Script"
---

 Among these tools, CSS Grid is among the most exciting and valuable. Whether you're building simple layouts or intricate designs, CSS Grid provides a new approach for better control and more efficient design.
In this article, we will explore the basics of CSS Grid, how it works, and compare it to Flexbox, another popular layout tool in CSS. This guide is designed for beginners, but we will also explore advanced concepts to give you a solid understanding of when and how to use CSS Grid in your web projects.
What Is CSS Grid?
CSS Grid Layout is a two-dimensional web layout system that allows web developers to design complex layouts easily using rows and columns. CSS Grid allows items to be aligned horizontally and vertically, unlike older layout techniques that required complicated calculations or manual adjustments.
At its core, CSS Grid allows you to define grid containers and grid items within them. You define rows and columns for the grid container and then place the items into specific grid areas. With CSS Grid, you can create fixed and flexible layouts, giving you fine-grained control over the design of your webpage.
Basic Syntax of CSS Grid
The basic syntax for using CSS Grid involves two main components: the grid container and the grid items.

1. Defining the Grid Container
To define a grid container, you must set the display property to grid or inline-grid. Once the container is defined, the child elements (grid items) can be placed into the grid.
Example:
.container {
  display: grid;
}
This simple declaration will turn the .container element into a grid container.
2. Defining Rows and Columns
Next, we define the number of rows and columns in the grid. You do this using the grid-template-rows and grid-template-columns properties, which specify the size of the rows and columns.
Example:
.container {
  display: grid;
  grid-template-columns: 100px 200px 300px;  /*Three columns with different widths */
  grid-template-rows: 150px 150px;          /* Two rows with fixed heights*/
}
Here, the grid will have three columns (with widths of 100px, 200px, and 300px) and two rows (both 150px tall).
3. Placing Grid Items
Once the grid is defined, you can place items into specific grid cells or areas. You can control the positioning of the grid items using properties like grid-column and grid-row.
Example:
.item1 {
  grid-column: 1 / 2;
  grid-row: 1 / 2;
}
In this example, .item1 will span from the first to the second column (covering the first column) and be placed in the first row.
Grid Tracks, Grid Cells, and Grid Lines
Before diving into more complex examples, it's essential to understand some basic concepts of CSS Grid:
Grid Tracks: The rows and columns that make up the grid. In the example above, grid-template-columns and grid-template-rows define the grid tracks.
Grid Cells: The individual spaces where grid items are placed. A grid cell intersects a grid row and a grid column.
Grid Lines: The lines that separate grid tracks. For example, in the declaration grid-template-columns: 100px 200px 300px, there are four grid lines—one before the first column, between the first and second, between the second and third, and after the third.
Advanced CSS Grid Features
CSS Grid offers several powerful features that make it incredibly flexible and helpful for complex layouts:
1.Grid Template Areas
A grid template area allows you to define the grid's layout using named areas. This can make your code more readable and easier to manage.
Example:
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-areas:
    "header header header"
    "main main sidebar"
    "footer footer footer";
}
In this example, we have named the grid areas (header, main, sidebar, footer). You can then assign items to these areas.
.header {
  grid-area: header;
}
.main {
  grid-area: main;
}
.sidebar {
  grid-area: sidebar;
}
.footer {
  grid-area: footer;
}
This approach makes it easier to visualize the layout and understand how each item is placed within the grid.
2.Auto Placement
CSS Grid also supports auto placement, automatically allowing the browser to position items based on available space. This is particularly useful for responsive layouts.
Example:
.container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
}
In this example, the grid will automatically adjust the number of columns based on the container's width. It will create as many 100px-wide columns as possible, and each column will grow to fill the available space.
Comparing CSS Grid and Flexbox
CSS Grid and Flexbox are powerful layout models in CSS, but they serve different purposes. Let's compare them and see when you might use one over the other.
1.One-Dimensional vs. Two-Dimensional Layouts
Flexbox: Flexbox is designed for one-dimensional layouts. It works well when you must arrange items in a single direction—a row or a column. It is excellent for layouts that require alignment and distribution along a single axis.
CSS Grid: CSS Grid is designed for two-dimensional layouts, allowing you to control rows and columns simultaneously. This makes CSS Grid perfect for more complex layouts, where you must align items horizontally and vertically.
2.Flexibility and Control
Flexbox: Flexbox gives you great flexibility for controlling the alignment, order, and distribution of items along the central axis (horizontally or vertically). However, it doesn't offer direct control over columns and rows simultaneously.
CSS Grid: CSS Grid gives you more control over the overall layout, including axes (rows and columns), making it ideal for creating complex grid-based designs.
3.Use Cases
Flexbox: Flexbox is ideal for more straightforward layouts or when you need to arrange items in a single direction, such as in navigation bars, card layouts, or forms.
CSS Grid: CSS Grid is better suited for complex web layouts, such as magazine-style designs, large-scale content grids, and responsive multi-column designs.
Practical Example: Responsive Web Layout with CSS Grid
Let's build a simple responsive webpage layout using CSS Grid.
HTML Structure:

< div class="container">
  < header class="header">Header</header>
  < main class="main">Main Content</main>
  < aside class="sidebar">Sidebar</aside>
  < footer class="footer">Footer</footer>
</div>
CSS for the Layout:
.container {
  display: grid;
  grid-template-columns: 1fr 3fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}

.header {
  grid-area: header;
}

.main {
  grid-area: main;
}

.sidebar {
  grid-area: sidebar;
}

.footer {
  grid-area: footer;
}
Responsive Adjustments:
We can adjust the number of columns at different screen sizes to make the layout responsive.
@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;
    grid-template-areas:
      "header"
      "main"
      "sidebar"
      "footer";
  }
}
In this example, the layout will switch to a single-column layout on smaller screens, stacking the elements on top of each other.
Conclusion
CSS Grid offers a compelling and flexible approach to web layout design. It allows you to create complex, responsive layouts with ease and precision. While Flexbox is excellent for more straightforward, one-dimensional layouts, CSS Grid excels in handling two-dimensional designs, making it a perfect tool for creating more intricate web layouts.
By understanding the fundamentals of CSS Grid and how it compares to Flexbox, you will be well on your way to mastering modern web layout techniques. As you practice and experiment, you'll find that CSS Grid opens up a world of possibilities for creating beautifully responsive and complex designs.

Happy coding!

\*\* Book Recommendation:

- [React and React Native: A complete hands-on guide to modern web and mobile development with React.js, 3rd Edition](https://amzn.to/3CStF7m)
- [React Key Concepts](https://amzn.to/43XOCJM)
- [Pragmatic Programmer](https://amzn.to/3W1P4oL) ***The: Your journey to mastery, 20th Anniversary Edition***

[Mentorship & Consulting - Contact us for more info](/contact)

***Join Our Discord Community*** [Unleash your potential, join a vibrant community of like-minded learners, and let's shape the future of programming together. Click here to join us on Discord.](https://discord.gg/A75tvDvZ)

***For Consulting and Mentorship, feel free to contact*** [slavo.io](/contact)
