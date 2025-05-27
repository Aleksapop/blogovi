---
title: "Building Navigation Bars with HTML and CSS"
date: "2025-03-20"
author: "Slavo"
image: "ts-big-o-notation.png"
excerpt: "Step-by-Step Guide to Creating Horizontal and Vertical Navigation Bars"
isFeatured: false
category: "Type Script"
---


As an experienced AI engineer, beginners often ask me how to get started with practical web development skills—especially when building AI-powered web apps. The navigation bar is one of the simplest, most essential components of any site or app. Whether you're building a portfolio site, a dashboard, or an AI tool, a solid nav bar is the key to good UX.
This article will explain the basics of creating horizontal and vertical navigation bars using only HTML and CSS. There are no frameworks or JavaScript—just raw, clean code.
Why Navigation Bars Matter
Navigation bars are one of the most essential components of any website or application. They play a critical role in shaping the user experience and ensuring users can find what they’re looking for quickly and easily. Here's why they matter:

1. Improve Usability and Accessibility
A well-designed navigation bar makes it easy for users to explore your site or app without confusion. It provides clear pathways to key pages or features, reducing frustration and improving user satisfaction. Accessible navigation (like keyboard-friendly menus and screen reader compatibility) is crucial for inclusivity for users with disabilities.
2. Set the Tone for Your App’s UI
The design, layout, and behavior of your navigation bar reflect the overall feel of your application. Whether it's minimalist, bold, modern, or playful—your navigation bar is often one of the first UI elements users interact with. It helps set expectations and build trust in your brand.
3. Provide Structure to Your Content
Navigation bars organize your content into logical sections and guide users through your site or app’s hierarchy. This structure helps users understand the relationship between different parts of your app, making the experience more intuitive and efficient.

🧱 What You’ll Learn
How to Structure a Navigation Bar with HTML
 Learn how to use semantic HTML elements such as < nav>, < ul>, < li>, and < a> to build a clean and accessible navigation bar. Understand how to organize navigation links to enhance the structure and usability of a website.
Styling Navigation Links with CSS
 Discover how to use CSS to style your navigation bar. You’ll learn to customize fonts, colors, spacing, hover effects, and active link states to create visually appealing and user-friendly navigation menus.
The Difference Between Horizontal and Vertical Nav Bars
 Explore the differences between horizontal and vertical navigation bars. Understand when to use each layout depending on your website’s design and user experience goals. Learn how to align items horizontally using Flexbox and stack them vertically with simple CSS.
Simple Responsive Tweaks
 Learn basic responsive design techniques to ensure your navigation bar looks great on all devices, from desktop to mobile. You’ll apply media queries and flexible layouts so that your nav bar adapts smoothly to different screen sizes.

## 🛠 Prerequisites

You don’t need any advanced knowledge to follow this tutorial. If you have a basic understanding of HTML and CSS, you're good to go!

---

## 📐 Horizontal Navigation Bar

We’ll start by building a horizontal navigation bar—this is commonly seen at the top of websites. It includes navigation links like Home, About, Projects, and Contact.

---

## 1. HTML Structure

Here’s the basic HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Horizontal Nav</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <nav class="navbar">
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Projects</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</body>
</html>
```

### What's Happening?

- The `<nav>` element is used for navigation content.
- Inside the `<nav>`, we use an unordered list (`<ul>`) to create menu items.
- Each `<li>` holds a link (`<a>`), which leads to different sections of the site.

---

## 2. CSS Styling

Here's the style file (`style.css`):

```css
/* style.css */

body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.navbar {
  background-color: #333;
}

.navbar ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex; /* Horizontal layout */
}

.navbar li {
  padding: 14px 20px;
}

.navbar a {
  color: white;
  text-decoration: none;
  display: block;
}

.navbar a: hover {
  background-color: #575757;
}
```

What's Happening?

- `display: flex` on the `ul` element makes the list items appear **horizontally**, side-by-side.
- We remove the default list styles (bullets, padding, margins).
- Each link is styled to look clean with no underlines and white text on a dark background.
- The `hover` effect changes the background when the user moves the mouse over a link.

---

## ✅ Result

You now have a **sleek horizontal navigation bar** at the top of your website. The links are evenly spaced and interactive.

---

## 🔁 Simple Responsive Tweaks

Let’s make this nav bar **mobile-friendly**. We want the links to stack vertically on small screens instead of being squeezed side-by-side.

### Add this to the bottom of your `style.css`

```css
@media screen and (max-width: 600px) {
  .navbar ul {
    flex-direction: column;
    align-items: flex-start;
  }

  .navbar li {
    width: 100%;
  }

  .navbar a {
    padding: 14px;
    width: 100%;
  }
}
```

### Explanation

- `@media screen and (max-width: 600px)` applies styles **only when the screen is 600px wide or smaller** (common on phones).
- `flex-direction: column` makes the nav items stack **vertically**.
- `width: 100%` ensures that each nav link stretches across the entire screen width for better usability on mobile.

---

## 🧪 Try it Out

Open your browser, resize the window, or use the Developer Tools (F12 → toggle device toolbar) to simulate a mobile screen.

## 🧭 Vertical Navigation Bar (Sidebar Navigation)

A vertical navigation bar, also known as a sidebar, is a fixed panel typically placed on the left side of the screen. It's commonly used in admin dashboards, web apps, or websites where space and navigation clarity are essential.

---

### ✅ 1. HTML Structure

This is the basic structure of the sidebar using HTML:

```html
<body>
  <nav class="sidebar">
    <ul>
      <li><a href="#">Dashboard</a></li>
      <li><a href="#">Reports</a></li>
      <li><a href="#">Settings</a></li>
      <li><a href="#">Logout</a></li>
    </ul>
  </nav>
</body>
```

Explanation

- `<nav>`: This semantic tag defines a navigation section.
- `.sidebar`: A class we'll use for styling the sidebar.
- `<ul>`: A list (`ul` stands for "unordered list") containing navigation links.
- Each `<li>` (list item) holds an `<a>` tag (a link to another page or section).

---

### 🎨 2. CSS Styling

This CSS code gives the sidebar its layout and design:

```css
.sidebar {
  width: 200px;               /* Sidebar width */
  height: 100vh;              /* Full viewport height */
  background-color: #222;     /* Dark background */
  position: fixed;            /* Fixed position so it stays on screen */
  top: 0;
  left: 0;
}

.sidebar ul {
  list-style-type: none;      /* Removes bullet points */
  padding: 0;                 /* No padding around the list */
  margin: 0;                  /* No margin */
}

.sidebar li {
  border-bottom: 1px solid #444;  /* Adds a subtle divider between items */
}

.sidebar a {
  display: block;             /* Links fill the entire list item */
  color: #fff;                /* White text color */
  padding: 15px 20px;         /* Padding inside each link */
  text-decoration: none;      /* Removes underline from links */
}

.sidebar a: hover {
  background-color: #444;     /* Darker background on hover */
}
```

#### Explanation of Key Styles

- `position: fixed;`: This makes the sidebar stay visible as the user scrolls.
- `height: 100vh;`: Ensures the sidebar fills the entire height of the screen.
- `: hover`: Adds an interactive hover effect when the user moves the mouse over a link.

---

### 🧪 Final Result

This will create a **clean, fixed vertical navigation bar** on the left side of the screen. It’s responsive to user interaction (hover effect) and provides a simple but effective way to organize links.
To make your navigation bar (navbar) responsive, you can use **CSS media queries**. These allow you to apply different styles depending on the screen size, ensuring your website looks great on large and small screens.

The following example demonstrates how to stack or collapse the navbar on smaller screens, typically mobile devices. We'll be using a **max-width** media query, which targets screen sizes of 768px or smaller (a common breakpoint for tablets and smartphones).

### Example Code

```css
@media (max-width: 768px) {
  /* Change the navigation list layout to be vertical (stacked) on smaller screens */
  .navbar ul {
    display: flex;
    flex-direction: column; /* Stacks the nav items vertically */
    align-items: center; /* Centers the items */
    padding: 0; /* Optional: removes default padding */
    margin: 0; /* Optional: removes default margin */
  }

  /* Adjust the sidebar to take full width and adjust height for small screens */
  .sidebar {
    width: 100%; /* Make the sidebar take up the entire width */
    height: auto; /* Allow height to adjust based on content */
    position: relative; /* Positioning the sidebar relative for stacking */
  }
}
```

Explanation

1. **Media Query (`@media (max-width: 768px)`)**: This tells the browser to apply the styles inside the curly braces only if the viewport width is 768px or less (typically mobile or tablet devices).

2. **Navbar Styling**:
   - `flex-direction: column;`: This changes the layout of the navbar's list items from a horizontal row (default) to a vertical stack.
   - `align-items: center;`: This ensures the navbar items are centered horizontally.

3. **Sidebar Styling**:
   - `width: 100%;`: On smaller screens, we want the sidebar to expand to the full width of the screen.
   - `height: auto;`: This ensures that the sidebar height adapts to its content instead of staying fixed.
   - `position: relative;`: This is often used for positioning the sidebar relative to other elements, allowing it to stack in a mobile-friendly way.

### How It Works

- The navbar will appear as a horizontal menu on screens wider than 768px (desktops, tablets, etc.).
- On screens smaller than 768px (smartphones), the navbar will stack vertically, and the sidebar will adjust to fill the screen.

This approach helps improve user experience on mobile devices by making the navigation easier to interact with.
🧠 From Basics to AI-Driven Interfaces
As someone deeply involved in AI development, small UI components form the foundation for building advanced, AI-powered tools. Whether you are:
Integrating an AI chatbot: AI chatbots are becoming increasingly common in customer service, personal assistants, and even sales. But to make them seamless, you need a user-friendly interface that ensures smooth interactions. A solid frontend foundation, from conversational UI elements to real-time response systems, is key.
Building a recommendation dashboard: Recommendation systems, like the ones used in e-commerce or media streaming platforms, rely on a robust UI to display personalized content. Frontend frameworks help structure complex data in a way that’s intuitive for users, from dynamic filtering to real-time suggestions, enhancing the user experience and engagement.
Hosting ML models on the web: Machine learning models offer powerful insights but need a clean and responsive interface to make them accessible to users. Strong frontend foundations ensure your AI models perform well in real-world web environments, whether you're displaying predictive analytics, interactive visualizations, or model outputs.
Integrating AI with frontend design requires a deep understanding of both fields in these scenarios. The front end is where AI interacts with the user, and a smooth, intuitive interface ensures that your advanced algorithms deliver their full potential. From designing dynamic components that respond to user inputs to providing real-time updates and a seamless flow of information, having a strong foundation in UI/UX design and frontend development is critical.
Ultimately, as AI tools become more complex, the interface will remain the critical point of contact between powerful backends (like machine learning models) and end users. A well-built interface will improve user experience and ensure that AI functionalities are effectively harnessed, making sophisticated systems more accessible and user-friendly.

Happy coding!

\*\* Book Recommendation:

- [React and React Native: A complete hands-on guide to modern web and mobile development with React.js, 3rd Edition](https://amzn.to/3CStF7m)
- [React Key Concepts](https://amzn.to/43XOCJM)
- [Pragmatic Programmer](https://amzn.to/3W1P4oL) **_The: Your journey to mastery, 20th Anniversary Edition_**

[Mentorship & Consulting - Contact us for more info](/contact)

**_Join Our Discord Community_** [Unleash your potential, join a vibrant community of like-minded learners, and let's shape the future of programming together. Click here to join us on Discord.](https://discord.gg/A75tvDvZ)

**_For Consulting and Mentorship, feel free to contact_** [slavo.io](/contact)
