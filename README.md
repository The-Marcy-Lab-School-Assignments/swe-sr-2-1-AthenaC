# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:
* Examples of semantic and non-semantic tags
* The differences between semantic and non-semantic tags
* The benefits of using semantic tags (when possible)

### Response 1
> ***Examples***
> * Semantic Tags: `<title>`, `<header>`, `<footer>`, `<h1>` 
> * Non-Semantic Tags: `<div>`, `<span>`, `<b>`, `<i>`, `<font>`
>
> **Differences:** 
> * ***Semantic tags*** are HTML elements that provide a clear distinction between each element being used and its contents. These tags help both developers and search engines understand the program they are maintaining or searching. For example, the `<header>` tag represents the header of a section or the entire page. Other semantic elements are self-explanatory or intuitive, making web development well-structured, organized, and meaningful.
> * ***Non-semantic tags*** do not provide information about the contents of the contained elements and are mainly used for layout and styling purposes. For example, the `<div>` tag is a versatile container used for grouping content or applying styles. A few other examples include `<b>` and `<i>`, which are used for text styling to create bold and italic text.
>
> **Benefits of Semantic Tags:** 
> * *Search Engine Optimization (SEO)* is the process of making a website more visible in search results, considering its content as important keywords to improve search rankings.
> * Semantic tags are friendly for visually impaired users using screen readers. They provide context by recognizing the roles of different elements, giving readers a better navigation experience.
> * Since semantic tags are easier to understand, they help developers find and manage blocks of code instead of sifting through non-descriptive tags. Semantic tags enhance accessibility, maintainability, and navigation in web development.
> * Semantic tags also help developers know what kind of program they are dealing with, indicating whether it involves HTML, CSS, or JavaScript. This clarity makes collaboration easier.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2
> It is important for developers to create websites that meet accessibility standards because they provide all users, especially those with disabilities, an easier way to navigate and interact with the site. Some effective ways to enhance accessibility include using semantic tags, providing alt text for images, ensuring keyboard navigation, maintaining good color contrast, implementing ARIA roles and landmarks, utilizing assistive technologies like VoiceOver, and choosing appropriate sizing units like `rem` over `px`.
> * *Semantic Tags:* Search engines use semantic tags, such as `<h1>` for headings, to index the structure and content of web pages. Similarly, users can skim through a page by its headings, aiding navigation and clarifying the document structure and relationships between sections.
> * *Alt Text for Images:* Alt text provides descriptive information for visually impaired users, ensuring they understand the content and context of images.
> * *Keyboard Navigation:* This ensures that interactive elements, like buttons, links, and forms, can be accessed and operated solely using the keyboard.
> * *Color Contrast:* Adequate color contrast between the background and text helps visually impaired users read content more easily.
> * *ARIA (Accessible Rich Internet Applications):* ARIA attributes allow developers to describe the state and role of elements, enhancing their accessibility. For instance, `role="button"` indicates that an element functions as a button, even if it isn’t a native `<button>` element. This assists assistive technologies in understanding the element's purpose.
> * *Landmarks:* Landmarks (also defined using ARIA roles) help users navigate the structure of web pages easily, enabling them to jump to different sections quickly.
> * *VoiceOver:* This is an assistive technology used on Apple devices for users who are blind or visually impaired. It reads aloud the text on the screen and provides auditory feedback about the interface.
> * *Rem (root em) vs. px (pixels):* Developers should consider accessibility when choosing sizing units. The rem unit is relative to the root element's font size, so if a user changes their browser's default font size, all elements sized with rem will scale proportionally. In contrast, pixels are an absolute unit of measurement that can lead to accessibility issues if users need larger text.

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;" >hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3
> It is useful to write inline styles for quick, small adjustments or testing during development. Inline styles allow you to immediately see the changes without having to switch back and forth between HTML and CSS files.
>
> However, writing styles in a separate CSS file promotes better organization, performance, and scalability, which are crucial for larger, maintainable web projects. Keeping HTML and CSS separate makes the code easier to read and maintain, and design changes don’t interfere with content. You can update styles without modifying the structure. An external CSS file allows you to apply the same styles across multiple pages, ensuring consistency and reducing redundancy—unlike inline styles, which require repetition on every element. External CSS files are cached by browsers, improving page load times, while inline styles must be processed with every page request, which can slow things down.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

* An explanation of the concept of "classes" and "ids" with an analogy.
* An example of the usage using an HTML code block and a CSS code block.
* An explanation of the syntax using the terms: **attribute**, **selector** 

### Response 4
> **The Concept of `Classes` and `IDs`:** `Classes` are like a category of books in the same genre, with multiple books sharing the same `class` of styling. `IDs` are like barcodes, unique to each book. In HTML/CSS, `classes` are used to denote multiple elements that will receive the same styling across the website, while `IDs` are unique and can apply to at most one element on the page, like a barcode.
> 
> ***Examples:***
> * *HTML:*
> ```html
> <p class="highlight">This is a highlighted paragraph.</p>
> <p id="unique-text">This paragraph has a unique ID.</p>
> ```
>
> * *CSS:*
> ```css
> /* Style all elements with class 'highlight' */
> .highlight {
>     color: blue;
>     font-weight: bold;
> }
> 
> /* Style the element with ID 'unique-text' */
> #unique-text {
>     color: green;
>     font-size: 20px;
> }
> ```
> 
> **HTML `class` Attribute:** An attribute is a property of an HTML element that provides additional information about that element. In the HTML example above, the `<p>` element has the attribute `class="highlight"`, meaning this paragraph belongs to the "highlight" `class`. The `class` is used when you want to style multiple elements in the same way. In this case, any other paragraphs with the `class` "highlight" would have the same blue, bold styling.
> 
> **HTML `id` Attribute:** The second `<p>` element has the attribute `id="unique-text"`, making this `id` unique to style this specific element.
>
> **CSS `class` Selector:** A selector is used to target HTML elements that match and apply styles to them. To select the `class` attribute in the CSS file, the period `.` before the `class` name tells the browser to style any element with that `class`.
> 
> **CSS `id` Selector:** The `#` symbol tells the browser to style the element with the exact `id` specified.

## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5
> HTML is used to provide the basic structure and skeleton of a webpage, such as headings, paragraphs, images, and lists. CSS is used for layout, styling, and animations, controlling how the content looks, such as colors, fonts, positioning, and hover effects. JavaScript is used for dynamic functionality and user interaction, such as handling user clicks, fetching data, and updating content. The DOM API allows JavaScript to manipulate the page's structure after the page is loaded. HTML/CSS should be used for structure and design, while JavaScript and the DOM API are used for interactivity and dynamic content. 

