---
title: "Building Multi-Page Websites: Linking Between Pages"
date: "2025-03-20"
author: "Slavo"
image: "ts-big-o-notation.png"
excerpt: "The world of web development is vast, and for anyone just beginning their journey, one essential concept is creating multi-page websites."
isFeatured: false
category: "Type Script"
---



The world of web development is vast, and for anyone just beginning their journey, one essential concept is creating multi-page websites. A multi-page website allows users to navigate from one page to another seamlessly. This skill is crucial for developers, especially when designing large websites or projects.
In this article, we will explore how to structure a multi-page website using HTML and CSS, link between different pages, and organize your project for efficiency. Whether you're working on a personal project, a business website, or any other digital experience, understanding multi-page websites will help you build scalable and user-friendly platforms.
What Is a Multi-Page Website?
Before diving into the technical aspects, let's define a multi-page website. As the name suggests, a multi-page website has several pages linked together to create a more significant, cohesive site. Each page serves a specific function or provides different content to the user. For example:
Homepage
About Page
Contact Page
Blog or Articles Section
Why Use a Multi-Page Website?
The benefits of multi-page websites are many:
Improved User Experience: With multiple pages, users can easily navigate content without feeling overwhelmed.
Better SEO (Search Engine Optimization): Each page can be optimized for specific keywords and topics, leading to better visibility on search engines.
Scalability: As the website grows, adding new pages is simple and does not disrupt the overall structure.
Organized Content: Information can be better categorized, making it easier for users to find what they want.
Understanding the Structure of a Multi-Page Website
A well-structured multi-page website will consist of the following core components:
HTML Files: These are the individual pages that make up the website. They contain the structure and content of your website.
CSS Files: This website style controls the appearance of HTML elements across all pages.
JavaScript Files: Optional, but these can add interactivity and dynamic content to your website.
Images and Media: Images, icons, and other media files are used on your site.
Assets Folder: You store your CSS, JavaScript, images, and fonts.
Setting Up the Folder Structure for Your Website
Proper folder organization is crucial for managing your files and ensuring your project is easy to navigate. Here's a typical structure:
/my-website
  /assets
    /css
      - styles.css
    /js
      - script.js
    /images
      - logo.png
  /index.html
  /about.html
  /contact.html
  /blog.html
In this structure:
The index.html is your homepage.
Each other .html file represents a page on your website.
The /assets folder holds files related to your website's design, such as CSS and JavaScript, as well as images.
Creating the Basic HTML Pages
Let's look at how to create a simple multi-page website using HTML. We will create a few basic pages: index.html, about.html, and contact.html.

1. index.html (Homepage)
This is the main page of your website, often the first page users see when they visit your site. It typically contains navigation links to other sections of your site.

<!DOCTYPE html>
< html lang="en">
< head>
    < meta charset="UTF-8">
    < meta name="viewport" content="width=device-width, initial-scale=1.0">
    < title>My Website</title>
    < link rel="stylesheet" href="assets/css/styles.css">
</head>
< body>
    < header>
        < nav>
            < ul>
                < li>< a href="index.html">Home</a></li>
                < li>< a href="about.html">About</a></li>
                < li>< a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <h1>Welcome to My Website</h1>
        <p>This is the homepage of my website. Here, you will find information about what we do and how you can get in touch.</p>
    </main>

    <footer>
        <p>&copy; 2025 My Website</p>
    </footer>
</body>
</html>
2. about.html (About Page)
The About page introduces your website or business. This page may include a history, mission statement, or other important information.
<!DOCTYPE html>
< html lang="en">
< head>
    < meta charset="UTF-8">
    < meta name="viewport" content="width=device-width, initial-scale=1.0">
    < title>About Us</title>
    < link rel="stylesheet" href="assets/css/styles.css">
</head>
< body>
    < header>
        < nav>
            < ul>
                < li>< a href="index.html">Home</a></li>
                < li>< a href="about.html">About</a></li>
                < li>< a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <h1>About Us</h1>
        <p>We are a company focused on providing innovative solutions to our customers. Learn more about our journey, values, and vision.</p>
    </main>

    <footer>
        <p>&copy; 2025 My Website</p>
    </footer>
</body>
</html>
3. contact.html (Contact Page)
The Contact page allows users to get in touch with you. This may include a contact form or your email address, phone number, or physical address.
<!DOCTYPE html>
< html lang="en">
< head>
    < meta charset="UTF-8">
    < meta name="viewport" content="width=device-width, initial-scale=1.0">
    < title>Contact Us</title>
    < link rel="stylesheet" href="assets/css/styles.css">
</head>
< body>
    < header>
        < nav>
            < ul>
                < li>< a href="index.html">Home</a></li>
                < li>< a href="about.html">About</a></li>
                < li>< a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <h1>Contact Us</h1>
        <p>If you have any questions, please get in touch with us via email or phone.</p>
        <form action="submit_contact_form" method="POST">
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name"><br>
            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email"><br>
            <input type="submit" value="Submit">
        </form>
    </main>

    <footer>
        <p>&copy; 2025 My Website</p>
    </footer>
</body>
</html>
Linking Between Pages
The key to creating a multi-page website is linking between pages. We have already used < a> (anchor) tags in the above examples to create hyperlinks. Here's a breakdown:
Anchor Tag (< a>) Syntax
< a href="page.html">Link Text</a>
The href attribute specifies the path to the page or section you want to link to.
The link text is the clickable content that appears on the webpage.
In the examples above, the navigation menu in the < header> contains links to the index.html, about.html, and contact.html pages. This allows users to navigate between different sections of the website.
Internal and External Links
You can create two types of links:
Internal Links: Links within the same website. For example, linking from the homepage to the About page.
Example: < a href="about.html">About Us</a>
External Links: Links to external websites. For example, linking to a third-party website.
Example: < a href="https://www.example.com" target="_blank">Visit Example</a>
Relative vs. Absolute Links
Relative Links: These links reference files within the same website.
Example: < a href="about.html">About</a>
Absolute Links: These links reference a full URL, including the domain.
Example: < a href="https://www.example.com">Visit Example</a>
For a local multi-page website, you will typically use relative links.
Styling Your Multi-Page Website
CSS is used to control the visual presentation of your website. You can link a single CSS file (like styles.css) to all your pages. Here's an example of a simple CSS file for styling:
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: #fff;
    padding: 10px;
    text-align: center;
}

nav ul {
    list-style-type: none;
}

nav ul li {
    display: inline;
    margin-right: 15px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: #333;
    color: #fff;
}
This CSS will style your header, navigation, and footer, giving a consistent look across all pages.
Best Practices for Multi-Page Websites
Keep URLs Descriptive: Use meaningful names for your HTML files. For example, use about.html instead of page2.html.
Organize Content: Group related content on separate pages. Don't overload any single page with too much information.
Consistency: Keep the navigation consistent across all pages so users know where they are at all times.
Mobile Responsiveness: Make sure your site looks good on all devices. Use CSS media queries to adjust the layout for different screen sizes.
SEO Optimization: Ensure each page is optimized for search engines with relevant titles, descriptions, and keywords.
Conclusion
Building a multi-page website involves more than just linking between pages. It's about creating a seamless, intuitive experience for users. By properly organizing your HTML, CSS, and assets, you can create a scalable website that is easy to maintain and grow.
Whether you're working on a personal project or a large-scale site, mastering the art of linking between pages and structuring your content will help you become an efficient web developer.
This article will provide the foundation for building more complex websites. As you continue your learning journey in AI and web development, remember that these fundamental skills will be essential as you integrate AI-driven features into your sites and applications.

Happy coding!

\*\* Book Recommendation:

- [React and React Native: A complete hands-on guide to modern web and mobile development with React.js, 3rd Edition](https://amzn.to/3CStF7m)
- [React Key Concepts](https://amzn.to/43XOCJM)
- [Pragmatic Programmer](https://amzn.to/3W1P4oL) **_The: Your journey to mastery, 20th Anniversary Edition_**

[Mentorship & Consulting - Contact us for more info](/contact)

**_Join Our Discord Community_** [Unleash your potential, join a vibrant community of like-minded learners, and let's shape the future of programming together. Click here to join us on Discord.](https://discord.gg/A75tvDvZ)

**_For Consulting and Mentorship, feel free to contact_** [slavo.io](/contact)
