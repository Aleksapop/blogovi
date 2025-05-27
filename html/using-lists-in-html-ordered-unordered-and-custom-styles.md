---
title: "Using Lists in HTML: Ordered, Unordered, and Custom Styles"
date: "2025-03-20"
author: "Slavo"
image: "ts-big-o-notation.png"
excerpt: "If you are beginning your journey into web development or artificial intelligence (AI), you might wonder why understanding HTML lists is essential."
isFeatured: false
category: "Type Script"
---

 As an experienced AI engineer and someone deeply engaged in creating platforms for learning AI, mastering the basics of HTML, including how to structure and style lists, lays a critical foundation for building more advanced applications.
Lists are a fundamental part of web development. They help structure content in a clean, semantic, and accessible way. Whether you're building an AI tutorial site, creating a personal blog, or designing an interface for displaying machine learning models and their performance metrics, lists come into play more often than expected.
In this article, we'll explore:
What HTML lists are
The differences between ordered and unordered lists
How to create and style these lists using CSS
How to create custom list styles
Best practices for using lists in modern web development
This in-depth guide (over 5500 words) is designed to help beginners understand the importance and versatility of HTML lists and how to harness CSS to make them look and function beautifully.

1. What Are Lists in HTML?
HTML (HyperText Markup Language) uses lists to display grouped items in a structured format. These lists can either be ordered (numbered), unordered (bulleted), or definition lists (term-description pairs).
Types of Lists:
Ordered List (< ol>)
Unordered List (< ul>)
Definition List (< dl>)
Each serves a different purpose and is applicable depending on the context.
Real-World Applications:
Ordered list: steps in a machine learning pipeline
Unordered list: features of a product
Definition list: glossary of AI terms
We'll dive into each type in the sections below.
2. Ordered Lists: Creating Step-by-Step Instructions
Syntax:

< ol>
  < li>Collect data</li>
  < li>Preprocess data</li>
  < li>Train the model</li>
  < li>Evaluate the model</li>
</ol>
Explanation:
The < ol> tag wraps the entire list, and each item is contained in an < li> (list item) tag. By default, ordered lists display numbers starting from 1.
Attributes:
type: changes the numbering style (1, A, a, I, i)
start: sets the starting number
reversed: displays list items in descending order
Example:
< ol type="A" start="3">
  < li>Input</li>
  < li>Processing</li>
  < li>Output</li>
</ol>
3. Unordered Lists: Grouping Items Without Order
Syntax:
< ul>
  < li>Python</li>
  < li>JavaScript</li>
  < li>TensorFlow</li>
  < li>PyTorch</li>
</ul>
Explanation:
Unordered lists use bullet points by default. These are ideal when the order of items doesn't matter.
Customizing Bullets:
By default, bullets are solid circles. CSS can be used to change the bullet style or custom images or icons.
4. Definition Lists: Displaying Term-Description Pairs
Syntax:
< dl>
  < dt>Supervised Learning</dt>
  < dd>A machine learning technique that uses labeled data.</dd>

  < dt>Unsupervised Learning</dt>
  < dd>A machine learning technique that finds patterns without labeled data.</dd>
</dl>
Explanation:
< dl>: definition list container
< dt>: definition term
< dd>: definition description
These are useful for glossaries, FAQs, or presenting structured information.
5. Styling Lists with CSS
Styling lists improves readability and adds visual appeal.
Common CSS Properties for Lists:
ul, ol {
  padding-left: 20px;
  margin-bottom: 1rem;
}

li {
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.6;
}
Removing Default Styles:
ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}
This is useful when you want complete control over how the bullets or numbers appear.
Customizing Bullet Points:
ul. custom-bullets li::before {
  content: '\2022'; /*Unicode for bullet*/
  color: #007BFF;
  font-weight: bold;
  display: inline-block;
  width: 1em;
  margin-left: -1em;
}
Using Images as Bullets:
ul. image-bullets {
  list-style: none;
}

ul. image-bullets li {
  background: url('bullet.png') no-repeat left center;
  padding-left: 25px;
  background-size: 15px;
}
6. Advanced List Styling Techniques
CSS Counters:
You can create fully customized ordered lists without using the default < ol> tag behavior.
.counter-list {
  counter-reset: section;
}

.counter-list li {
  counter-increment: section;
  list-style: none;
}

.counter-list li::before {
  content: counter(section) ". ";
  font-weight: bold;
  color: #333;
}
Multi-column Lists:
.multi-column {
  column-count: 2;
  column-gap: 30px;
}
Responsive List Design:
Use media queries to adapt the list style for different screen sizes.
@media (max-width: 600px) {
  ul, ol {
    padding-left: 10px;
    font-size: 14px;
  }
}
7. Accessibility Best Practices
Always use semantic tags (< ul>, < ol>, < dl>) correctly.
Avoid using lists purely for layout.
Provide sufficient color contrast.
Use ARIA roles if necessary (e.g., role= "list" for dynamic content).
8. Lists in Real AI Projects
In AI-focused applications, lists appear in:
Model performance dashboards
Step-by-step AI pipelines
Displaying features or datasets
Glossaries and term explainers
Example:
< ol>
  < li>Collect dataset from Kaggle</li>
  < li>Preprocess using pandas</li>
  < li>Train model using scikit-learn</li>
  < li>Visualize metrics using matplotlib</li>
</ol>
9. Tools and Frameworks That Leverage Lists
React/JSX: Use .map() to dynamically generate lists
Bootstrap: Provides pre-styled list groups
Tailwind CSS: Utility-first list styling
Markdown to HTML converters: Automatically transform - and 1. into HTML lists
Example (React):
const steps = ['Collect data,' 'Clean data,' 'Train model'];
return (
  < ol>
    {steps.map((step, index) => < li key={index}>{step}</li>)}
  </ol>
);
10. Common Mistakes and How to Avoid Them
Nesting block elements like < div> inside < li> improperly
Forgetting to close < li> tags
Using < ul> for ordered content and vice versa
Ignoring accessibility or responsive design
Mastering HTML lists and their CSS styling is essential in any web developer's toolkit, especially for those venturing into AI and educational platforms. Lists are more than bullet points or numbers—powerful structuring tools that improve UX, accessibility, and clarity.
Whether you're documenting a machine learning pipeline, listing the benefits of your AI product, or building a glossary for your AI learners, using the correct list type and styling it well will set your work apart.
In the next phase of your learning, consider experimenting with frameworks like React, exploring accessibility tools, or even generating list content dynamically using AI!
Happy coding!

Happy coding!

\*\* Book Recommendation:

- [React and React Native: A complete hands-on guide to modern web and mobile development with React.js, 3rd Edition](https://amzn.to/3CStF7m)
- [React Key Concepts](https://amzn.to/43XOCJM)
- [Pragmatic Programmer](https://amzn.to/3W1P4oL) ***The: Your journey to mastery, 20th Anniversary Edition***

[Mentorship & Consulting - Contact us for more info](/contact)

***Join Our Discord Community*** [Unleash your potential, join a vibrant community of like-minded learners, and let's shape the future of programming together. Click here to join us on Discord.](https://discord.gg/A75tvDvZ)

***For Consulting and Mentorship, feel free to contact*** [slavo.io](/contact)
