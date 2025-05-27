---
title: "Introduction to CSS Layout: Flexbox"
date: "2025-03-20"
author: "Slavo"
image: "ts-big-o-notation.png"
excerpt: "CSS Flexbox (Flexible Box) is a powerful layout model designed to create responsive and flexible web page layouts."
isFeatured: false
category: "Type Script"
---

 It simplifies the arrangement of elements, making it easier to build dynamic user interfaces without relying on floats or positioning hacks. If you're starting your AI journey and working on front-end development, understanding Flexbox is crucial to creating modern, responsive designs.
**What is Flexbox?**

Flexbox, short for Flexible Box Layout, is a CSS layout model designed to facilitate the design of flexible and efficient layouts within a container. It is beneficial to distribute space among items and align them properly, even when their size is unknown or dynamic.

Unlike traditional CSS layouts that are based on block (vertical) and inline (horizontal) flows, Flexbox is one-dimensional. This means it works either in a row (horizontal axis) or a column (vertical axis), but not both simultaneously. This makes it ideal for building responsive layouts that adjust smoothly to different screen sizes and content lengths.

---

### Key Features of Flexbox

1. **Main Axis and Cross Axis**  
   - The **main axis** is the primary direction in which flex items are laid out (e.g., left to right in a row).
   - The **cross axis** is perpendicular to the central axis (e.g., top to bottom if the central axis is a row).

2. **Flex Container and Flex Items**  
   - A **flex container** is an element with `display: flex` or `display: inline-flex`.
   - The direct children of this container become **flex items**, which are automatically arranged according to the rules of the Flexbox layout.

3. **Flexible Sizing**  
   - Items can grow, shrink, or stay fixed depending on the available space using properties like `flex-grow`, `flex-shrink`, and `flex-basis`.

4. **Alignment and Justification**  
   - Flexbox allows you to **align items horizontally** (`justify-content`) and **vertically** (`align-items`, `align-self`, `align-content`) easily.

5. **Reordering Elements**  
   - You can change the visual order of flex items without altering the HTML structure using the `order` property.

---

### Common Flexbox Properties

#### On the container

- `display: flex` – Activates flexbox layout.
- `flex-direction` – Defines the direction of the central axis (`row`, `row-reverse`, `column`, `column-reverse`).
- `justify-content` – Aligns items along the main axis.
- `align-items` – Aligns items along the cross axis.
- `flex-wrap` – Allows items to wrap onto multiple lines.

#### On the items

- `flex` – A shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.
- `align-self` – Overrides `align-items` for individual items.
- `order` – Controls the order in which items appear.

---

### Example

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
```

```html
<div class="container">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
```

In this example, the three items are arranged in a horizontal row, spaced evenly, and vertically centered within the container.

### 🔑 **Key Concepts of Flexbox**

Flexbox, or the Flexible Box Layout, is a CSS layout model designed to arrange elements in a single dimension—either as a row or a column. It provides a more efficient way to align, distribute, and space items within a container, especially when their size is dynamic or unknown.

---

### 1. **Flex Container**

The **flex container** is the **parent** element that holds all the flex items. To activate Flexbox, you apply:

```css
.container {
    display: flex;
}
```

This changes the behavior of all the direct child elements (flex items), giving you access to powerful alignment and spacing tools.

#### Common properties for the Flex Container

- `flex-direction`: Defines the direction of the central axis (row or column).
- `justify-content`: Aligns items along the central axis (left to right by default).
- `align-items`: Aligns items along the cross axis (top to bottom by default).
- `flex-wrap`: Allows items to wrap onto multiple lines.

---

### 2. **Flex Items**

**Flex items** are the **direct children** of a flex container. Once Flexbox is enabled, these items can grow, shrink, and align flexibly.

#### Common properties for Flex Items

- `flex`: A shorthand for setting `flex-grow`, `flex-shrink`, and `flex-basis`.
- `align-self`: Overrides `align-items` for individual items.
- `order`: Changes the visual order of the flex items, regardless of their HTML position.
- `flex-grow`: Defines how much a flex item will grow relative to the others.
- `flex-shrink`: Defines how much a flex item will shrink if needed.
- `flex-basis`: Sets the initial size of a flex item before the remaining space is distributed.

---

Example

```html
<div class="container">
  <div class="item">One</div>
  <div class="item">Two</div>
  <div class="item">Three</div>
</div>
```

```css
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.item {
    flex: 1;
    padding: 10px;
}
```

## 🔹 1. `flex-direction`

The `flex-direction` property defines the main axis of the flex container—this is the direction in which flex items are laid out.

**Values:**

- `row` *(default)* – Items are placed from **left to right**, in a horizontal line.
- `row-reverse` – Items are placed from **right to left**.
- `column` – Items are placed from **top to bottom**, in a vertical stack.
- `column-reverse` – Items are placed from **bottom to top**.

**Example:**

```css
.container {
    display: flex;
    flex-direction: row;
}
```

📝 When you change the `flex-direction`, you change how items flow inside the container. If you're designing vertical layouts, `column` might make more sense.

---

## 🔹 2. `justify-content`

The `justify-content` property controls **how items are aligned along the central axis**, depending on the `flex-direction`.

**Values:**

- `flex-start` *(default)* – Items are aligned to the **start** of the main axis.
- `flex-end` – Items are aligned to the **end** of the central axis.
- `center` – Items are **centered** along the main axis.
- `space-between` – Items are **evenly spaced**, with the first item at the start and the last at the end.
- `space-around` – Items have **equal space around** them. Half-sized space on the ends.
- `space-evenly` – Items are spaced with **equal space between and around** all items.

**Example:**

```css
.container {
    display: flex;
    justify-content: center;
}
```

📝 Use this to control how items are **spaced horizontally** (if `flex-direction` is `row`) or **vertically** (if `flex-direction` is `column`).

---

## 🔹 3. `align-items`

The `align-items` property controls **how items are aligned along the cross axis** (the axis perpendicular to the main one).

**Values:**

- `flex-start` – Items are aligned to the **start** of the cross axis (top if `row,` left if `column`).
- `flex-end` – Items are aligned to the **end** of the cross-axis.
- `center` – Items are **centered** along the cross axis.
- `stretch` *(default)* – Items **stretch** to fill the container’s cross axis (if no fixed height/width).
- `baseline` – Items are aligned so their **text baselines line up**.

**Example:**

```css
.container {
    display: flex;
    align-items: center;
}
```

### 🔹 `flex-grow` – Controls How Items Grow

The `flex-grow` property defines **how much a flex item should grow** relative to the other items inside the same flex container **when there is extra space** available along the central axis.

- **Default value**: `0` (items will not grow by default).
- **Example**:

  ```css
  .item {
      flex-grow: 1;
  }
  ```

  This means the item will take up **an equal share of the available extra space** with other items that also have `flex-grow: 1`.

- If one item has `flex-grow: 2` and another has `flex-grow: 1`, the first will get **twice as much extra space** as the second.

---

### 🔹 `flex-shrink` – Controls How Items Shrink

The `flex-shrink` property determines **how much a flex item should shrink** relative to the other items **when there isn't enough space** in the flex container.

- **Default value**: `1` (items will shrink if needed).
- **Example**:

  ```css
  .item {
      flex-shrink: 1;
  }
  ```

  This means that when there is not enough space, the item will shrink at the same rate as other items with the same `flex-shrink` value.

- If one item has `flex-shrink: 2` and another has `flex-shrink: 1`, the first item will shrink **twice as much** as the second one.

- Set it to `0` if you **don't want the item to shrink** at all.

---

### 🔹 `flex-basis` – Sets the Initial Size

The `flex-basis` property defines the **initial size of the flex item** before any growing or shrinking occurs.

- **Default value**: `auto` (size based on content or width/height if set).
- **Example**:

  ```css
  .item {
      flex-basis: 100px;
  }
  ```

  This means the item will be **100 pixels broad** (or tall, depending on the flex direction) before applying flex-grow or flex-shrink rules.

- Think of it as a starting point for the item's size.

---

### Bonus: The Shorthand – `flex`

You can combine all three properties using the `flex` shorthand:

```css
.item {
    flex: 1 1 100px; /* flex-grow flex-shrink flex-basis */
}
```

Or simply:

```css
.item {
    flex: 1; /* equivalent to 1 1 0 */
}
```

### 🌟 Creating a Simple Flexbox Layout

#### HTML Structure

```html
<div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
</div>
```

This code creates a container that holds three child elements, each labeled "Item 1", "Item 2", and "Item 3".

---

#### CSS Styling

```css
.container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 200px;
    background-color: lightgray;
}

.item {
    width: 100px;
    height: 100px;
    background-color: steelblue;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
}
```

##### Explanation

- **`.container { display: flex; }`**  
  Turns the container into a **flex container**, enabling Flexbox properties on its children (the `.item` elements).

- **`justify-content: space-around;`**  
  Distributes the space **evenly around** the items. That means equal spacing is added on the left and right of each item.

- **`align-items: center;`**  
  Aligns the items **vertically centered** within the container’s height.

- **`height: 200px;`**  
  Sets the container’s height so that we can see the vertical alignment.

- **`.item` styles**  
  - Each item is a square (100px by 100px) with a blue background.
  - The text is centered horizontally and vertically using Flexbox again (`display: flex`, `justify-content: center`, `align-items: center`).

---

### 💡 Why Use Flexbox?

Flexbox (short for **Flexible Box Layout**) is a powerful CSS layout module that provides more efficient ways to align and distribute space among elements in a container.

Here are the key benefits:

#### ✅ Simplifies Complex Layouts  

Flexbox allows you to build dynamic and complex layouts with minimal code. No more floating elements or using table-based designs.

#### ✅ Makes Responsive Design Easier  

It automatically adjusts the size and position of items based on the screen size, making your layout more responsive across devices.

#### ✅ Eliminates Floats and Positioning Hacks  

Before Flexbox, developers had to rely on floating elements or tricky margin/padding combinations. Flexbox simplifies this by providing built-in alignment tools.

#### ✅ Better Alignment and Spacing Control  

With properties like `justify-content`, `align-items`, and `flex-grow`, you have full control over how items are aligned, spaced, and sized—both horizontally and vertically.

Happy coding!

\*\* Book Recommendation:

- [React and React Native: A complete hands-on guide to modern web and mobile development with React.js, 3rd Edition](https://amzn.to/3CStF7m)
- [React Key Concepts](https://amzn.to/43XOCJM)
- [Pragmatic Programmer](https://amzn.to/3W1P4oL) ***The: Your journey to mastery, 20th Anniversary Edition***

[Mentorship & Consulting - Contact us for more info](/contact)

***Join Our Discord Community*** [Unleash your potential, join a vibrant community of like-minded learners, and let's shape the future of programming together. Click here to join us on Discord.](https://discord.gg/A75tvDvZ)

***For Consulting and Mentorship, feel free to contact*** [slavo.io](/contact)
