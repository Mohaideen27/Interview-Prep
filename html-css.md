Absolutely! Since you are a fresher preparing for a Frontend Developer interview, I'll help you prepare from the basics.

My goal is not just to give you definitions to memorize. I want you to understand each concept so that you can confidently explain it to an interviewer.

We'll prepare all 43 HTML and CSS questions in an interview-friendly format.

### How you should prepare

For every question, I'll provide:

1. Simple explanation – Easy to understand.
2. Interview answer – What you can say to the interviewer.
3. Example – Where necessary, with code.
4. Important point – Something extra that can help you stand out.

# Part 1: HTML interview questions

## 1. What is HTML?

Simple explanation:

HTML stands for HyperText Markup Language. It is used to create the structure of web pages.

It tells the browser what content should be displayed, such as headings, paragraphs, images, links, tables, and forms.

Interview answer:

"HTML stands for HyperText Markup Language. It is the standard markup language used to create the structure of web pages. It uses different tags and elements to organize content like headings, paragraphs, images, links, and forms."

Example:

```
<!DOCTYPE html>
<html>
<head>
    <title>My First Page</title>
</head>
<body>
    <h1>Welcome</h1>
    <p>This is my first webpage.</p>
</body>
</html>
```

Remember: HTML creates the structure, CSS handles styling, and JavaScript adds functionality.

## 2. What is HTML5?

Simple explanation:

HTML5 is the modern version of HTML. It introduced new elements and features that help developers create modern websites.

Some important HTML5 features are:

- Semantic tags like `header`, `footer`, and `article`.
- Audio and video support.
- Canvas for drawing graphics.
- Local storage and session storage.
- Improved form input types.

Interview answer:

"HTML5 is the fifth major version of HTML. It introduced semantic elements, multimedia support, improved forms, and browser storage features, making web development easier and more powerful."

Example:

```
<header>
    <h1>My Website</h1>
</header>

<main>
    <section>
        <h2>About Us</h2>
        <p>Welcome to our website.</p>
    </section>
</main>

<footer>
    <p>Copyright 2026</p>
</footer>
```

## 3. What is the difference between HTML and HTML5?

Interview answer:

"HTML is the markup language used to create web page structures, whereas HTML5 is a newer version of HTML that introduced semantic elements, multimedia support, better forms, and browser storage features."

| HTML (older versions)                | HTML5                                      |
| ------------------------------------ | ------------------------------------------ |
| Limited semantic elements            | Supports semantic elements                 |
| Multimedia often required plugins    | Supports audio and video                   |
| Limited form input types             | New input types like email and date        |
| No standard Web Storage API          | Supports localStorage and sessionStorage   |
| Less support for modern web features | Better support for modern web applications |

## 4. What are HTML tags and elements?

Simple explanation:

- Tag: A keyword enclosed within angle brackets.
- Element: The complete structure, including opening tag, content, and closing tag (when applicable).

Example:

```
<p>Hello World</p>
```

Here:

- `<p>` is the opening tag.
- `Hello World` is the content.
- `</p>` is the closing tag.
- The complete structure is the paragraph element.

Interview answer:

"An HTML tag is the markup used to define the beginning or end of an element. An HTML element consists of the opening tag, content, and closing tag. Some elements, like images and line breaks, are void elements and don't have closing tags."

## 5. What is the difference between block-level and inline elements?

Block-level elements:

- Start on a new line.
- Usually occupy the available width of their parent container.
- Can have width and height set.

Examples: `div`, `p`, `h1`, `section`.

Inline elements:

- Do not normally start on a new line.
- Take only the space their content needs.
- Width and height generally do not apply in the normal inline formatting model.

Examples: `span`, `a`, `strong`, `em`.

Example:

```
<div>This is block 1</div>
<div>This is block 2</div>

<span>Inline 1</span>
<span>Inline 2</span>
```

Interview answer:

"Block-level elements start on a new line and generally take the full available width, whereas inline elements stay in the same line and occupy only the space required by their content."

## 6. What are semantic HTML elements?

Simple explanation:

Semantic elements are HTML elements that clearly describe the meaning of their content.

Examples:

| Element   | Purpose                 |
| --------- | ----------------------- |
| `header`  | Header section          |
| `nav`     | Navigation links        |
| `main`    | Main page content       |
| `section` | A section of content    |
| `article` | Independent content     |
| `aside`   | Related or side content |
| `footer`  | Footer section          |

Example:

```
<header>
    <h1>My Website</h1>
</header>

<nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
</nav>

<main>
    <article>
        <h2>HTML Basics</h2>
        <p>Learn HTML step by step.</p>
    </article>
</main>

<footer>
    Copyright 2026
</footer>
```

Interview answer:

"Semantic HTML elements clearly describe the meaning and purpose of the content. Examples include header, nav, main, section, article, and footer. They improve code readability, accessibility, and SEO."

## 7. What is the difference between div and span?

| div                              | span                               |
| -------------------------------- | ---------------------------------- |
| Block-level by default           | Inline by default                  |
| Starts on a new line             | Stays in the same line             |
| Used to group larger sections    | Used to group small inline content |
| Takes available width by default | Takes content width by default     |

Example:

```
<div>
    <h2>Welcome</h2>
    <p>Hello everyone!</p>
</div>

<p>My name is <span>John</span>.</p>
```

Interview answer:

"Both div and span are non-semantic container elements. Div is a block-level element used to group larger sections, whereas span is an inline element used to style or group small portions of text."

## 8. What is the purpose of the DOCTYPE declaration?

Simple explanation:

DOCTYPE tells the browser which HTML standard the document follows and helps the browser render the page in standards mode.

Example:

```
<!DOCTYPE html>
```

This declaration is used in HTML5.

Interview answer:

"DOCTYPE stands for Document Type Declaration. It tells the browser to render the document using standards mode. In HTML5, we use a simple declaration: `<!DOCTYPE html>`."

Important: DOCTYPE is not an HTML tag.

## 9. What are attributes in HTML?

Simple explanation:

Attributes provide additional information about HTML elements.

They are usually written inside the opening tag.

Example:

```
<a href="https://example.com" target="_blank">
    Visit Website
</a>
```

Here:

- `href` specifies the link destination.
- `target="_blank"` opens the link in a new tab.

Other examples:

- `id`
- `class`
- `src`
- `alt`
- `href`
- `type`
- `placeholder`

Interview answer:

"HTML attributes provide additional information about elements. They are written inside the opening tag and usually consist of a name and a value."

## 10. What is the difference between id and class?

| id                                   | class                                |
| ------------------------------------ | ------------------------------------ |
| Should be unique within a page       | Can be reused                        |
| Selected using `#` in CSS            | Selected using `.` in CSS            |
| An element should have one unique ID | An element can have multiple classes |
| Used for unique identification       | Used for grouping similar elements   |

Example:

```
<h1 id="heading">Welcome</h1>

<p class="text">Hello</p>
<p class="text">Welcome back</p>
```

```
#heading {
    color: blue;
}

.text {
    color: green;
}
```

Interview answer:

"ID is used to uniquely identify an element, whereas class is used to group multiple elements for applying common styles or behavior. In CSS, ID uses the hash symbol and class uses the dot symbol."

## 11. What are forms in HTML?

Simple explanation:

HTML forms are used to collect information from users, such as names, email addresses, passwords, and phone numbers.

Interview answer:

"HTML forms are used to collect user input and send that information to a server. We use the form tag along with input, label, textarea, select, and button elements."

Example:

```
<form action="/submit" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

    <label for="email">Email:</label>
    <input type="email" id="email" name="email">

    <button type="submit">Submit</button>
</form>
```

Important attributes:

- `action`: Specifies where the form data is sent.
- `method`: Specifies how the data is sent.
- `name`: Identifies the form field when submitting data.
- `required`: Makes a field mandatory.

## 12. What are the different input types in HTML?

Simple explanation:

HTML provides different input types to collect different kinds of information from users.

Important input types:

| Input type | Purpose                         |
| ---------- | ------------------------------- |
| `text`     | Accepts text                    |
| `password` | Accepts passwords               |
| `email`    | Accepts email addresses         |
| `number`   | Accepts numbers                 |
| `tel`      | Accepts telephone numbers       |
| `date`     | Selects a date                  |
| `radio`    | Selects one option from a group |
| `checkbox` | Selects multiple options        |
| `file`     | Uploads files                   |
| `submit`   | Submits a form                  |
| `reset`    | Resets form values              |
| `button`   | Creates a clickable button      |
| `url`      | Accepts a URL                   |
| `range`    | Selects a value using a slider  |
| `color`    | Selects a color                 |

Example:

```
<form>
    <input type="text" placeholder="Enter name">
    <input type="email" placeholder="Enter email">
    <input type="password" placeholder="Enter password">

    <input type="radio" name="gender" value="male"> Male
    <input type="radio" name="gender" value="female"> Female

    <input type="checkbox"> I agree

    <button type="submit">Submit</button>
</form>
```

Interview answer:

"HTML provides different input types such as text, password, email, number, radio, checkbox, date, and file. Each input type is used to collect a particular type of user information."

## 13. What is the difference between GET and POST methods?

Simple explanation:

GET and POST are HTTP methods used to communicate with a server.

- GET is mainly used to retrieve data.
- POST is mainly used to submit data or create resources.

Interview answer:

"GET is used to request data from a server, and its parameters are commonly passed through the URL. POST is used to send data in the request body. GET requests can be bookmarked and cached in typical situations, whereas POST requests are generally used for submitting sensitive or larger amounts of data. However, POST alone does not provide security; HTTPS is required to protect data in transit."

| GET                               | POST                                              |
| --------------------------------- | ------------------------------------------------- |
| Mainly retrieves data             | Mainly submits data                               |
| Parameters commonly appear in URL | Data is sent in request body                      |
| Can be bookmarked                 | Cannot normally be bookmarked with submitted data |
| Can be cached                     | Not cached by default                             |
| Should not change server state    | Can change server state                           |
| URL length limitations apply      | No equivalent URL parameter limitation            |

Example:

```
<!-- GET -->
<form method="GET" action="/search">
    <input type="text" name="query">
    <button type="submit">Search</button>
</form>

<!-- POST -->
<form method="POST" action="/register">
    <input type="text" name="username">
    <button type="submit">Register</button>
</form>
```

## 14. What is the purpose of the label tag?

Simple explanation:

The `label` tag gives a name or description to an input field.

It also makes the input easier to use because clicking the label can focus or activate its associated input.

Example:

```
<label for="email">Email:</label>
<input type="email" id="email">
```

Here, `for="email"` connects the label to the input having `id="email"`.

Interview answer:

"The label tag is used to describe form controls. It improves accessibility and usability because screen readers can identify the purpose of the input, and users can click the label to interact with the associated field."

## 15. What is the difference between required, readonly, and disabled?

| required                        | readonly                                  | disabled                                       |
| ------------------------------- | ----------------------------------------- | ---------------------------------------------- |
| Makes a field mandatory         | Prevents users from editing the value     | Prevents users from interacting with the field |
| User can enter a value          | User can view and usually focus the field | Usually cannot focus the field                 |
| Participates in form validation | Not subject to required validation        | Excluded from form submission                  |
| Submitted if valid and named    | Submitted if named                        | Not submitted                                  |

Example:

```
<input type="text" required>

<input type="text" value="John" readonly>

<input type="text" value="John" disabled>
```

Interview answer:

"Required makes an input mandatory, readonly allows users to view the value but not modify it, and disabled makes the input inactive. A key difference is that readonly fields are submitted with the form, but disabled fields are not."

## 16. What is the purpose of local storage?

Simple explanation:

Local storage is a browser feature used to store data on the user's device.

The stored data remains available even after closing and reopening the browser, until it is removed.

Example:

```
// Store data
localStorage.setItem("username", "John");

// Get data
let name = localStorage.getItem("username");

// Remove one item
localStorage.removeItem("username");

// Clear all data for the origin
localStorage.clear();
```

Interview answer:

"Local storage is a browser storage mechanism that allows us to store key-value pairs in the user's browser. The data persists even after the browser is closed and reopened. It is commonly used for storing preferences and other non-sensitive information."

Important: Local storage stores values as strings. It is not suitable for sensitive information such as passwords or authentication secrets.

## 17. What is the difference between localStorage, sessionStorage, and cookies?

| Feature                      | localStorage           | sessionStorage                    | Cookies                          |
| ---------------------------- | ---------------------- | --------------------------------- | -------------------------------- |
| Storage                      | Browser                | Browser                           | Browser                          |
| Lifetime                     | Until manually removed | Until the tab's page session ends | Based on expiry settings         |
| Capacity                     | Usually around 5–10 MB | Usually around 5–10 MB            | Usually around 4 KB per cookie   |
| Sent to server automatically | No                     | No                                | Yes, when applicable             |
| Common use                   | User preferences       | Temporary tab data                | Sessions and server-related data |

Interview answer:

"Local storage stores data permanently until it is manually removed. Session storage stores data for a particular browsing session, generally until the tab is closed. Cookies store small pieces of data and can be automatically sent to the server with matching requests."

Example:

```
localStorage.setItem("theme", "dark");

sessionStorage.setItem("page", "home");

document.cookie = "username=John; path=/";
```

## 18. What is the purpose of the meta viewport tag?

Simple explanation:

The viewport tag helps websites display correctly on different screen sizes, especially mobile devices.

Example:

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

- `width=device-width`: Sets the viewport width to the device width.
- `initial-scale=1.0`: Sets the initial zoom level to 100%.

Interview answer:

"The meta viewport tag is used to control the viewport dimensions and scaling of a webpage. It is important for responsive web design because it helps the page display properly on mobile devices."

## 19. How do you embed images, audio, and video in HTML?

Simple explanation:

HTML provides specific tags to display images and play audio and video files.

Image:

```
<img src="photo.jpg" alt="A beautiful landscape">
```

Audio:

```
<audio controls>
    <source src="music.mp3" type="audio/mpeg">
</audio>
```

Video:

```
<video controls width="400">
    <source src="video.mp4" type="video/mp4">
</video>
```

Interview answer:

"We use the img tag to display images, the audio tag to embed audio files, and the video tag to embed video files. The controls attribute provides playback controls to users."

Important: Always provide meaningful alternative text for informative images.

## 20. What is accessibility in HTML?

Simple explanation:

Accessibility means designing websites so that everyone can use them, including people with disabilities.

For example, a visually impaired person may use a screen reader to understand a webpage.

Important accessibility practices:

1. Use semantic HTML elements.
2. Add `alt` text to meaningful images.
3. Use labels for form inputs.
4. Make websites keyboard-friendly.
5. Use proper heading order.
6. Provide sufficient color contrast.
7. Use meaningful link text.

Example:

```
<img src="logo.png" alt="Company logo">

<label for="username">Username:</label>
<input type="text" id="username">

<button type="submit">Submit</button>
```

Interview answer:

"Accessibility in HTML means creating websites that can be used by everyone, including people with disabilities. We can improve accessibility by using semantic elements, alt attributes, proper labels, keyboard navigation, and appropriate heading structures."

# Part 2: CSS interview questions

## 1. What is CSS?

Simple explanation:

CSS stands for Cascading Style Sheets. It is used to style HTML elements and make websites visually attractive.

With CSS, we can control:

- Colors
- Fonts
- Backgrounds
- Spacing
- Layouts
- Animations
- Responsive designs

Interview answer:

"CSS stands for Cascading Style Sheets. It is used to control the presentation and appearance of HTML elements. We use CSS to add colors, fonts, layouts, spacing, animations, and responsive designs to websites."

Example:

```
<h1>Hello World</h1>
```

```
h1 {
    color: blue;
    font-size: 30px;
    text-align: center;
}
```

## 2. What are the different ways to apply CSS?

There are three main ways to apply CSS.

1\. Inline CSS

CSS is written directly inside the HTML element using the `style` attribute.

```
<h1 style="color: red;">Hello World</h1>
```

2\. Internal CSS

CSS is written inside the `style` tag in the HTML document.

```
<head>
    <style>
        h1 {
            color: blue;
        }
    </style>
</head>
```

3\. External CSS

CSS is written in a separate `.css` file and connected using the `link` tag.

HTML:

```
<link rel="stylesheet" href="style.css">
```

CSS:

```
h1 {
    color: green;
}
```

Interview answer:

"There are three ways to apply CSS: inline CSS, internal CSS, and external CSS. Inline CSS is written inside an HTML element, internal CSS is written inside a style tag, and external CSS is written in a separate CSS file. External CSS is generally preferred because it improves code organization and reusability."

## 3. What is the CSS box model?

Simple explanation:

The CSS box model explains how every HTML element is represented as a rectangular box.

It consists of four parts:

[Box Model Demystified: Margin, Border, Padding & Content - Euron Daily | Euron Community](https://images.openai.com/static-rsc-4/aNhJ5Hv9YEE0LLuFCrQxMEDQ_IPKsc85eHhW6jgkh1zwJmushl24aMsEIfzZ-IBueplaLN4JEmixTRp5c4x0W5xoEd_awQCsUM_soM1dg3XTeGKNvuWjldtPtK3xRPEZG3XYVu6RLJtWWmE16OvBHxsAIugXrPIUK_szeuHn_9k?purpose=inline)

[euron.one](https://euron.one/community/posts/d14457ca-5699-4307-bef0-889364028e4c?utm_source=chatgpt.com)

1. Content: Actual text, image, or other content.
2. Padding: Space between content and border.
3. Border: Line surrounding the padding and content.
4. Margin: Space outside the border.

Example:

```
.box {
    width: 200px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
```

With the default `content-box` model, the total width is:

200 + 40 + 10 = 250px (excluding margins).

Interview answer:

"The CSS box model describes how an element's size is calculated. It consists of content, padding, border, and margin. Every HTML element follows the box model."

Important: We commonly use `box-sizing: border-box` to include padding and border within the specified width and height.

```
* {
    box-sizing: border-box;
}
```

## 4. Explain margin, padding, and border.

Margin: Space outside the element's border.

Padding: Space between the content and the border.

Border: The line surrounding the content and padding.

Example:

```
.box {
    margin: 20px;
    padding: 15px;
    border: 2px solid black;
}
```

Interview answer:

"Margin creates space outside an element, padding creates space inside an element between its content and border, and border surrounds the content and padding."

## 5. What is the difference between margin and padding?

| Margin                                           | Padding                         |
| ------------------------------------------------ | ------------------------------- |
| Space outside the border                         | Space inside the border         |
| Separates elements                               | Creates space around content    |
| Background does not extend into margin           | Background extends into padding |
| Can have negative values                         | Cannot have negative values     |
| Vertical margins can collapse in some situations | Padding does not collapse       |

Example:

```
.box {
    margin: 20px;
    padding: 10px;
}
```

Interview answer:

"Margin is used to create space outside an element, whereas padding is used to create space between the content and the border of an element."

## 6. What is the difference between display: block, inline, and inline-block?

| Block                            | Inline                                | Inline-block                   |
| -------------------------------- | ------------------------------------- | ------------------------------ |
| Starts on a new line             | Stays in the same line                | Stays in the same line         |
| Takes available width by default | Takes content width                   | Takes content width by default |
| Width and height can be set      | Width and height do not work normally | Width and height can be set    |
| Example: div                     | Example: span                         | Example: styled span           |

Example:

```
.block {
    display: block;
}

.inline {
    display: inline;
}

.inline-block {
    display: inline-block;
    width: 150px;
    height: 50px;
}
```

Interview answer:

"Block elements start on a new line and take the available width by default. Inline elements stay in the same line and take only the required content space. Inline-block elements stay in the same line while allowing us to set width and height."

## 7. What is Flexbox?

Simple explanation:

Flexbox is a CSS layout system used to arrange elements in a row or column.

It makes it easier to align items, distribute space, and create flexible layouts.

Important Flexbox properties:

| Property          | Purpose                              |
| ----------------- | ------------------------------------ |
| `display: flex`   | Enables Flexbox                      |
| `flex-direction`  | Sets row or column direction         |
| `justify-content` | Aligns items along the main axis     |
| `align-items`     | Aligns items along the cross axis    |
| `flex-wrap`       | Allows items to move to another line |
| `gap`             | Adds space between items             |
| `align-content`   | Aligns multiple flex lines           |

Example:

```
<div class="container">
    <div class="box">One</div>
    <div class="box">Two</div>
    <div class="box">Three</div>
</div>
```

```
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
}
```

[Basic FlexBox - DEV Community](https://images.openai.com/static-rsc-4/XlHvAK7DHmSOZ1n4fhZYfiAJ5cydbh5_bR0stxopKA9QEkzQBoE90Yihgw9uCft-6PUbkyqeTm1BRe3eP7cFm2wNjVs28Isq-o_Vjcv9QBCOlaYvUsnZRcZI7hoLh9grt12xUMY-hugR1lS6Bi45diyojp3BJqsQtdxnpfCof5w?purpose=inline)

[dev.to](https://dev.to/ajwerth/basic-flexbox-4738?utm_source=chatgpt.com)

Interview answer:

"Flexbox is a one-dimensional CSS layout system used to arrange elements in a row or column. It helps us align items, distribute available space, and create flexible layouts using properties like justify-content, align-items, and flex-direction."

Important interview point:

- Main axis depends on `flex-direction`.
- Cross axis is perpendicular to the main axis.
- `justify-content` works along the main axis.
- `align-items` works along the cross axis.

## 8. What is CSS Grid?

Simple explanation:

CSS Grid is a two-dimensional layout system used to create rows and columns.

It is useful for creating complex website layouts.

Example:

```
<div class="container">
    <div>One</div>
    <div>Two</div>
    <div>Three</div>
    <div>Four</div>
</div>
```

```
.container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
}
```

[CSS Grid - 4 Squares Layout | Foundation 6](https://images.openai.com/static-rsc-4/ElREeD9JYX8SLEpyeZn9sXpwgQFfKjgCzhS3M3pEAv-gvprDtYA5jgY1Uzg_8k13eElj7_OiYLBQpVIslr8igIvo6ndEQ4hniFdQHoKLzXyAOM8NdYfVttDrwdlL3xeC6KCvidxAY8upM6g5cMmAfo-KXUkwUGEVyK8fARwJ5Ug?purpose=inline)

[get.foundation](https://get.foundation/building-blocks/blocks/four-squares-layout.html?utm_source=chatgpt.com)

Important Grid properties:

- `display: grid`
- `grid-template-columns`
- `grid-template-rows`
- `gap`
- `grid-column`
- `grid-row`
- `justify-items`
- `align-items`

Interview answer:

"CSS Grid is a two-dimensional layout system that allows us to create layouts using rows and columns. It is useful for creating complex page structures and responsive layouts."

## 9. What is the difference between Flexbox and Grid?

| Flexbox                           | Grid                             |
| --------------------------------- | -------------------------------- |
| One-dimensional layout            | Two-dimensional layout           |
| Works with rows or columns        | Works with rows and columns      |
| Best for component alignment      | Best for page-level layouts      |
| Content-driven layouts are common | Layout-driven designs are common |
| Uses `display: flex`              | Uses `display: grid`             |

Example:

Flexbox:

```
.container {
    display: flex;
    gap: 10px;
}
```

Grid:

```
.container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
}
```

Interview answer:

"Flexbox is mainly used for one-dimensional layouts, either rows or columns, whereas Grid is used for two-dimensional layouts involving both rows and columns. We can use both together in the same project."

Real-world examples:

- Flexbox: Navigation bar, buttons, card alignment.
- Grid: Dashboard, image gallery, website layout.

## 10. What is the difference between relative, absolute, fixed, and sticky positioning?

CSS provides five position values, but these four are especially important.

| Position   | Explanation                                                       |
| ---------- | ----------------------------------------------------------------- |
| `relative` | Positions an element relative to its normal position              |
| `absolute` | Positions an element relative to its nearest positioned ancestor  |
| `fixed`    | Positions an element relative to the viewport                     |
| `sticky`   | Behaves normally until a scroll threshold is reached, then sticks |

Example:

```
.parent {
    position: relative;
}

.child {
    position: absolute;
    top: 10px;
    right: 10px;
}

.navbar {
    position: fixed;
    top: 0;
}

.header {
    position: sticky;
    top: 0;
}
```

Interview answer:

"Relative positioning moves an element from its normal position without removing its original space. Absolute positioning removes the element from normal document flow and positions it relative to its nearest positioned ancestor. Fixed positioning keeps an element at a fixed position relative to the viewport, while sticky positioning switches between normal and fixed-like behavior during scrolling."

Important: An absolutely positioned element does not always use the viewport as its reference. It uses its nearest positioned ancestor when one exists.

## 11. What are pseudo-classes?

Simple explanation:

Pseudo-classes are used to style an element based on its state or position.

They use a single colon `:`.

Common pseudo-classes:

- `:hover`
- `:active`
- `:focus`
- `:first-child`
- `:last-child`
- `:nth-child()`
- `:checked`
- `:disabled`

Example:

```
button:hover {
    background-color: blue;
    color: white;
}

input:focus {
    border: 2px solid green;
}
```

Interview answer:

"Pseudo-classes are CSS keywords used to style elements based on their state or position. For example, hover applies styles when the mouse pointer is over an element, and focus applies styles when an element receives focus."

## 12. What are pseudo-elements?

Simple explanation:

Pseudo-elements are used to style a specific part of an element or insert generated content.

They generally use double colons `::`.

Common pseudo-elements:

- `::before`
- `::after`
- `::first-letter`
- `::first-line`
- `::selection`
- `::placeholder`

Example:

```
h1::before {
    content: "★ ";
    color: orange;
}

p::first-letter {
    font-size: 30px;
    color: red;
}
```

Interview answer:

"Pseudo-elements are used to style specific parts of an element or create generated content without adding extra HTML elements. Examples include before, after, first-letter, and first-line."

Remember:

- Pseudo-class: `:hover`
- Pseudo-element: `::before`

## 13. What is CSS specificity?

Simple explanation:

CSS specificity determines which CSS rule is applied when multiple rules target the same element and conflict with each other.

Specificity order (highest to lowest):

1. Inline styles
2. ID selectors
3. Class, attribute, and pseudo-class selectors
4. Element and pseudo-element selectors

Example:

```
<p id="title" class="text">Hello World</p>
```

```
p {
    color: green;
}

.text {
    color: blue;
}

#title {
    color: red;
}
```

Final color: Red

Because the ID selector has higher specificity than the class and element selectors.

Interview answer:

"CSS specificity is the system used by browsers to determine which CSS rule takes priority when multiple rules target the same element. Inline styles generally have higher specificity than IDs, classes, and element selectors. The `!important` declaration can override normal cascade priority, but it should be used carefully."

Extra point: When specificity is equal, the rule that comes later in the cascade generally wins, assuming the same origin and importance.

## 14. What is the difference between em, rem, %, and px?

Simple explanation:

These are CSS units used to define sizes, spacing, and dimensions.

| Unit  | Meaning                                                                                        |
| ----- | ---------------------------------------------------------------------------------------------- |
| `px`  | CSS pixels                                                                                     |
| `em`  | Relative to the font size of the relevant parent or current element, depending on the property |
| `rem` | Relative to the root element's font size                                                       |
| `%`   | Relative to the reference value defined by the property                                        |

Example:

```
html {
    font-size: 16px;
}

.parent {
    font-size: 20px;
}

.child {
    font-size: 2em;
    width: 50%;
}

.heading {
    font-size: 2rem;
}
```

Here:

- `2em` for the child font size = 40px.
- `2rem` = 32px.
- `50%` width = half of the containing block's width (in this example).

Interview answer:

"Pixels are fixed CSS units, em is relative to a relevant font size, rem is relative to the root element's font size, and percentage is relative to another reference value, often the parent or containing block."

## 15. What are media queries?

Simple explanation:

Media queries are used to apply different CSS styles depending on the device or screen characteristics.

They are very useful for responsive web design.

Example:

```
.container {
    width: 80%;
}

@media (max-width: 768px) {
    .container {
        width: 100%;
    }
}
```

Here, when the viewport width is 768px or smaller, the container width becomes 100%.

Interview answer:

"Media queries are a CSS feature that allows us to apply different styles based on screen size, device characteristics, and other conditions. They are mainly used to make websites responsive."

Common breakpoints used in practice:

- Mobile: around 320–480px.
- Tablet: around 481–768px.
- Desktop: above 768px.

These are common starting points, not mandatory standards.

## 16. How do you make a website responsive?

Simple explanation:

Responsive web design means creating websites that adjust to different screen sizes, such as mobile phones, tablets, and desktops.

Important techniques:

1. Use the viewport meta tag.
2. Use flexible layouts with Flexbox and Grid.
3. Use media queries.
4. Use relative units like `%`, `rem`, and `fr`.
5. Use responsive images.
6. Avoid fixed widths where flexible sizing is more suitable.

Example:

```
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

@media (max-width: 768px) {
    .container {
        grid-template-columns: 1fr;
    }
}
```

Interview answer:

"To make a website responsive, I use flexible layouts like Flexbox and Grid, media queries, relative units, and responsive images. I also include the viewport meta tag so the website adjusts properly to different device screen sizes."

## 17. What is the difference between visibility: hidden and display: none?

| visibility: hidden                  | display: none                       |
| ----------------------------------- | ----------------------------------- |
| Hides the element                   | Hides the element                   |
| Keeps its original layout space     | Removes its layout space            |
| Element is not normally interactive | Element is not normally interactive |
| Other elements retain its space     | Other elements can occupy its space |

Example:

```
.box1 {
    visibility: hidden;
}

.box2 {
    display: none;
}
```

Interview answer:

"Visibility hidden hides an element but keeps its space in the layout, whereas display none completely removes the element from the layout, so other elements can occupy that space."

## 18. What is the difference between z-index and position?

Simple explanation:

- `position` controls how an element is placed in the document.
- `z-index` controls the stacking order of overlapping elements.

Example:

```
.box1 {
    position: relative;
    z-index: 1;
}

.box2 {
    position: relative;
    z-index: 2;
}
```

If these elements overlap within the same stacking context, box2 appears above box1.

Interview answer:

"Position controls the positioning behavior of an element, while z-index controls its stacking order when elements overlap. A higher z-index generally appears above a lower one within the same stacking context."

Important: `z-index` is not simply a global ranking. Stacking contexts can affect which element appears on top.

## 19. What are CSS transitions and animations?

CSS Transitions:

Transitions make changes in CSS properties happen smoothly when a property changes.

Example:

```
button {
    background-color: blue;
    transition: background-color 0.5s ease;
}

button:hover {
    background-color: red;
}
```

CSS Animations:

Animations allow us to create more complex movements and effects using keyframes.

Example:

```
.box {
    animation: move 2s infinite;
}

@keyframes move {
    from {
        transform: translateX(0);
    }

    to {
        transform: translateX(100px);
    }
}
```

Interview answer:

"CSS transitions are used to create smooth changes between property values, usually when an event like hover occurs. CSS animations use keyframes to create more complex animations that can run automatically and repeat."

| Transition                             | Animation                    |
| -------------------------------------- | ---------------------------- |
| Usually triggered by a property change | Can start automatically      |
| Uses transition properties             | Uses keyframes               |
| Suitable for simple effects            | Suitable for complex effects |
| Has start and end states               | Can have multiple keyframes  |

## 20. What is Tailwind CSS?

Simple explanation:

Tailwind CSS is a utility-first CSS framework.

Instead of writing separate CSS classes for every design, we use predefined utility classes directly in HTML.

Example using normal CSS:

```
<button class="my-button">Click Me</button>
```

```
.my-button {
    background-color: blue;
    color: white;
    padding: 10px 20px;
    border-radius: 5px;
}
```

The same using Tailwind CSS:

```
<button class="bg-blue-500 text-white px-5 py-2 rounded">
    Click Me
</button>
```

Interview answer:

"Tailwind CSS is a utility-first CSS framework that provides predefined utility classes for styling HTML elements. It helps developers build responsive user interfaces quickly without writing separate CSS for every component."

[Tailwind CSS：ユーティリティファーストのスタイリング革命｜がらむまさら](https://images.openai.com/static-rsc-4/QfqRxeP1Q-6XwRenbHp2mw-i1JHh6Xn5kzcsfVEDbjO3lIWiPyqBf6-TgOi4JDnqcmrch9Go307O0lvu1t7StYFE3-Weub0oIoIql3ZylDseXzagpad1MLEAC6O4-bXPgnq3aGUQGeI82_DZWeg0hkJpO8o6JSmioFPGoCD7ljM?purpose=inline)

[note.com](https://note.com/lepandaivre/n/n4c0ddf8c20bf?utm_source=chatgpt.com)

## 21. What are the advantages of Tailwind CSS?

Important advantages:

1. Faster development.
2. Reusable utility classes.
3. Easy responsive design.
4. Consistent design system.
5. Less need to write custom CSS.
6. Easy customization through configuration and design tokens.
7. Unused styles can be excluded from production builds by the build process.

Interview answer:

"The main advantages of Tailwind CSS are faster development, consistent styling, responsive design utilities, and less need to write custom CSS. It also makes it easier to maintain a consistent design system across a project."

## 22. What is the difference between normal CSS and Tailwind CSS?

| Normal CSS                               | Tailwind CSS                           |
| ---------------------------------------- | -------------------------------------- |
| We write custom CSS rules                | We use predefined utility classes      |
| Styles are usually in CSS files          | Classes are written directly in markup |
| Requires creating and managing selectors | Reduces the need for custom selectors  |
| More freedom in naming and organization  | Follows a utility-first approach       |
| Useful for any custom design             | Useful for rapid UI development        |

Example:

Normal CSS:

```
<div class="card">Hello</div>
```

```
.card {
    background: white;
    padding: 20px;
    border-radius: 10px;
}
```

Tailwind CSS:

```
<div class="bg-white p-5 rounded-xl">
    Hello
</div>
```

Interview answer:

"In normal CSS, we write our own selectors and styling rules in CSS files. In Tailwind CSS, we use predefined utility classes directly in HTML. Both can achieve the same design, but Tailwind often makes styling faster and more consistent."

## 23. How do you handle responsive layouts using Tailwind CSS?

Simple explanation:

Tailwind CSS provides responsive prefixes that allow us to apply different styles at different screen sizes.

Common responsive prefixes:

| Prefix | Default minimum width |
| ------ | --------------------- |
| `sm:`  | 640px                 |
| `md:`  | 768px                 |
| `lg:`  | 1024px                |
| `xl:`  | 1280px                |
| `2xl:` | 1536px                |

These are the default breakpoints and can be customized.

Example:

```
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">

    <div class="bg-blue-500 p-4">Card 1</div>

    <div class="bg-green-500 p-4">Card 2</div>

    <div class="bg-red-500 p-4">Card 3</div>

</div>
```

Explanation:

- Mobile: One column.
- Medium screens (768px and above): Two columns.
- Large screens (1024px and above): Three columns.

Interview answer:

"Tailwind CSS uses responsive prefixes like sm, md, lg, xl, and 2xl. These allow us to apply different utility classes based on screen width. For example, we can display one column on mobile, two columns on tablets, and three columns on desktop."

# Part 3: Important practical questions for freshers

Interviewers often ask you to write small HTML and CSS programs instead of only explaining definitions.

Make sure you can do these without looking at the answers.

## HTML practical tasks

- Create a registration form.
- Create a login form.
- Create a table with rows and columns.
- Create an ordered and unordered list.
- Add an image with alternative text.
- Create radio buttons and checkboxes.
- Create a dropdown using `select` and `option`.
- Create a webpage using semantic HTML tags.

## CSS practical tasks

- Center a div horizontally and vertically.
- Create a navigation bar using Flexbox.
- Create a two-column layout using Grid.
- Create a responsive card layout.
- Create a button hover effect.
- Create a simple login page.
- Create a sticky navbar.
- Create a circular profile image.
- Create a simple CSS animation.

# Part 4: Your 7-day interview preparation plan

Your preparation tracker

0/7 completed

Day 1: HTML basics

Questions 1–10 and basic HTML structure.

Day 2: HTML advanced

Questions 11–20 and create a registration form.

Day 3: CSS fundamentals

Questions 1–6 and box model practice.

Day 4: CSS layouts

Flexbox, Grid and positioning.

Day 5: CSS advanced

Questions 11–19, responsive design and media queries.

Day 6: Tailwind CSS

Questions 20–23 and build a responsive card layout.

Day 7: Mock interview

Revise all questions and practise coding without help.

# Part 5: Let's practise a real interview!

My suggestion is that you don't just read all 43 answers. Practise answering them in your own words.

I'll act as your interviewer. I'll ask one question at a time, evaluate your answer, correct your mistakes, and give you a better interview-ready answer.

Mock interview

Question 1 of 5

# What is HTML?

Imagine you are sitting in front of the interviewer. Answer in your own words.

Need a hint?Submit answer

PreviousNext question

One important piece of advice: As a fresher, you are not expected to know everything. Interviewers mainly want to see that your fundamentals are clear, you can explain concepts in simple language, and you can write basic code yourself.

Let's aim to make you confident in HTML, CSS, JavaScript and practical frontend development, one step at a time!
