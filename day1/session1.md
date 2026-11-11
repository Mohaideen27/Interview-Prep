# Day 1 – Session 1: HTML & CSS Interview Preparation

Today's session covers the foundation of frontend development. We'll study each topic from basic concepts → practical examples → interview questions → hands-on exercises.

Your resume lists HTML, CSS and Tailwind CSS as frontend skills, and your projects use React.js. So we'll focus on concepts you should be able to explain and demonstrate in a React development interview.&#x20;

MohaideenResume2026.pdf



Today's session

Session 1

# 3–3.5 hours

# 45 min

HTML fundamentals

# 45 min

CSS fundamentals

# 45 min

Layout and responsiveness

# 45 min

Tailwind and interview practice

## Part 1 – HTML elements and semantic tags

### 1. What is HTML?

HTML stands for HyperText Markup Language.

It is used to create the structure of a web page.

For example, consider an e-commerce website:

- HTML creates the product title.
- HTML displays product images.
- HTML creates buttons.
- HTML creates forms.
- HTML structures navigation menus.

HTML is not a programming language. It is a markup language.

### 2. Basic HTML document structure

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">
    <title>My Website</title>
</head>
<body>

    <h1>Welcome to My Website</h1>
    <p>This is my first webpage.</p>
    <button>Click Me</button>

</body>
</html>
```

Understand each part:

| Element           | Purpose                 |
| ----------------- | ----------------------- |
| `<!DOCTYPE html>` | Declares HTML5 document |
| `<html>`          | Root element            |
| `<head>`          | Contains metadata       |
| `<title>`         | Browser tab title       |
| `<body>`          | Visible webpage content |
| `<h1>`            | Main heading            |
| `<p>`             | Paragraph               |

### 3. What are HTML elements?

An HTML element generally consists of:

- Opening tag
- Content
- Closing tag

Example:

```
<p>Hello World</p>
```

Here:

- `<p>` is the opening tag.
- `Hello World` is the content.
- `</p>` is the closing tag.

Some elements are void elements and don't need closing tags, such as:

```
<img src="photo.jpg" alt="Photo">
<br>
<hr>
<input type="text">
```

### 4. What are semantic HTML elements?

Semantic elements clearly describe their meaning to browsers and developers.

[10 semantic HTML tags to better structure your website](https://images.openai.com/static-rsc-4/GIZn7T9W70aIdrF4rAn9Dd30Up2X31B_1iH8ssUvFsmAsd43bwioDwhSZ823bmny3LtVpLz_XUdXqsji9ErMxsP2gSqKfnqw6PudrXLZO0i1KZxrRcXRSp_50MjggJmoUMdGLO_IiPp4GZ8zPfoOagkgWEEANIWneU3RtQ57eNA?purpose=inline)

[hartenfeller.dev](https://hartenfeller.dev/blog/underused-semantic-html-tags?utm_source=chatgpt.com)

Important semantic tags:

| Tag            | Purpose                      |
| -------------- | ---------------------------- |
| `<header>`     | Header section               |
| `<nav>`        | Navigation links             |
| `<main>`       | Main page content            |
| `<section>`    | Thematic content section     |
| `<article>`    | Independent content          |
| `<aside>`      | Related or side content      |
| `<footer>`     | Footer section               |
| `<figure>`     | Self-contained media content |
| `<figcaption>` | Media caption                |

Example:

```
<header>
    <h1>ShopSphere</h1>

    <nav>
        <a href="/">Home</a>
        <a href="/products">Products</a>
        <a href="/contact">Contact</a>
    </nav>
</header>

<main>
    <section>
        <h2>Our Products</h2>

        <article>
            <h3>Mobile Phone</h3>
            <p>Price: ₹15,000</p>
        </article>
    </section>
</main>

<footer>
    <p>Copyright 2026 ShopSphere</p>
</footer>
```

Interview question: What is the difference between semantic and non-semantic elements?

Answer:

Semantic elements clearly describe their purpose, such as `header`, `nav`, `article` and `footer`.

Non-semantic elements like `div` and `span` do not describe their meaning. They are mainly used as general containers.

### 5. HTML forms and input types

Forms collect information from users.

Example:

```
<form>
    <label for="username">Username:</label>

    <input
        type="text"
        id="username"
        name="username"
        required
    >

    <label for="email">Email:</label>

    <input
        type="email"
        id="email"
        name="email"
        required
    >

    <label for="password">Password:</label>

    <input
        type="password"
        id="password"
        name="password"
    >

    <button type="submit">Register</button>
</form>
```

Important input types:

| Input type | Usage               |
| ---------- | ------------------- |
| text       | Text input          |
| password   | Password            |
| email      | Email address       |
| number     | Numeric input       |
| tel        | Telephone number    |
| date       | Date selection      |
| radio      | Single selection    |
| checkbox   | Multiple selections |
| file       | File upload         |
| submit     | Form submission     |
| search     | Search input        |
| url        | Website URL         |
| time       | Time selection      |
| range      | Slider              |

Important interview questions

1. What is an HTML form?
2. What is the difference between GET and POST?
3. What is the difference between radio buttons and checkboxes?
4. What is the difference between readonly and disabled?
5. What is the purpose of the `required` attribute?
6. What is the purpose of the `name` attribute?
7. What is the difference between button and submit?
8. What is HTML form validation?

## Part 2 – Block vs Inline elements

### Block-level elements

Block elements generally start on a new line and occupy the available horizontal space.

Examples:

```
<div>Hello</div>
<p>Welcome</p>
<h1>Heading</h1>
<section>Content</section>
```

### Inline elements

Inline elements generally occupy only the space required by their content.

Examples:

```
<span>Hello</span>
<a href="#">Click here</a>
<strong>Important</strong>
<em>Highlighted</em>
```

[Understanding HTML Tags and Elements - Coder Legion](https://images.openai.com/static-rsc-4/pVhpm_7mJcB3_3LxsGVC1AmCTbZr7mX4fCAnnt38fHPnt1_VRI8e83L33OC8TqcsBwHBO2Bc5uK7Ul6X640wo5tDK8wC-frleP-Nw0a-ez9VsVl9PsQi0htRQ_bUvnMlCzY9wJGScgUQRt5Zm1Gi8J8cXbHpBUt11ExsPS4vcww?purpose=inline)

[coderlegion.com](https://coderlegion.com/12901/understanding-html-tags-and-elements?utm_source=chatgpt.com)

### Difference

| Block                         | Inline                                 |
| ----------------------------- | -------------------------------------- |
| Starts on a new line          | Stays within the same line             |
| Usually takes available width | Takes content width                    |
| Width and height can be set   | Width and height generally don't apply |
| Examples: div, p              | Examples: span, a                      |

Important: `display: inline-block` combines characteristics of both. It stays inline but supports width and height.

### Interview question

Q: Can we convert a block element into an inline element?

Answer: Yes. We can use CSS.

```
div {
    display: inline;
}
```

Similarly:

```
span {
    display: block;
}
```

## Part 3 – CSS Box Model

The CSS box model is one of the most frequently asked frontend interview topics.

Every HTML element is represented as a rectangular box.

[Difference Between Margin and Padding: A CSS Guide](https://images.openai.com/static-rsc-4/drGB_mrLKWS5PLWqJQZN-YcGNRgPziTcqTHVYdEvuDlSGQt96rxNaJeOKF55aEnbMXXi5AmHQJrKwJvTeWOWfbdmyLZNkrR-W71gUywVK3DGkSvDK_NGGAzesGqyC55JFPQPRNOZArdcEB5C3hogfAiEJ2xN4uSA8Dj0LddVMxk?purpose=inline)

[codedesign.ai](https://codedesign.ai/blog/difference-between-margin-and-padding/?utm_source=chatgpt.com)

It consists of four parts:

1. Content – Actual text, image or other content.
2. Padding – Space between content and border.
3. Border – Boundary around the element.
4. Margin – Space outside the border.

Example:

```
.box {
    width: 200px;
    height: 100px;

    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
```

With the default `content-box` sizing:

- Content width = 200px
- Left and right padding = 40px
- Left and right border = 10px
- Total width = 250px

### What is box-sizing?

```
* {
    box-sizing: border-box;
}
```

With `border-box`, the declared width includes content, padding and border.

For example, if width is 200px, the total width remains 200px.

Interview questions

1. Explain the CSS box model.
2. What is the difference between margin and padding?
3. What is `box-sizing`?
4. What is the difference between content-box and border-box?
5. Does margin affect the actual element width?
6. What is margin collapsing?

## Part 4 – CSS Flexbox

Flexbox is a CSS layout system used to arrange elements in a row or column.

It is especially useful for:

- Navigation bars.
- Aligning items.
- Centering content.
- Product cards.
- Buttons and menus.

[- Exclusive Addons](https://images.openai.com/static-rsc-4/MSDaCH5obvN7BpyLXNoDqB5gf8bDgZNW_98sCnI72FyWra2aJ_YkCSDWVMTfscj7D-OsUe7OQwfbbDVjFR4O6LFox1VI-e6hD04ef3YlQsnehOP3EZW7q9yfCVbImNJi_ZrG5yNhOz-8UyKcmYnBqefdFeRrKIwH6niLOEVd9u0?purpose=inline)

[exclusiveaddons.com](https://exclusiveaddons.com/flexible-container/?utm_source=chatgpt.com)

### 1. How to enable Flexbox?

```
.container {
    display: flex;
}
```

The element becomes a flex container, and its direct children become flex items.

### 2. Important Flexbox properties

| Property          | Purpose                       |
| ----------------- | ----------------------------- |
| `display: flex`   | Enables Flexbox               |
| `flex-direction`  | Sets row or column            |
| `justify-content` | Aligns items along main axis  |
| `align-items`     | Aligns items along cross axis |
| `flex-wrap`       | Allows items to wrap          |
| `gap`             | Adds spacing                  |
| `align-content`   | Aligns multiple flex lines    |

### 3. Example: Center a div

```
<div class="container">
    <div class="box">Hello World</div>
</div>
```

```
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 300px;
}
```

This centers the box horizontally and vertically.

### 4. Understanding justify-content

```
.container {
    display: flex;
    justify-content: space-between;
}
```

Common values:

- `flex-start`
- `flex-end`
- `center`
- `space-between`
- `space-around`
- `space-evenly`

### 5. Understanding flex-direction

```
.container {
    display: flex;
    flex-direction: row;
}
```

Values:

- row
- row-reverse
- column
- column-reverse

Interview questions

1. What is Flexbox?
2. What is a flex container?
3. What is a flex item?
4. What is the difference between justify-content and align-items?
5. What is flex-direction?
6. What is flex-wrap?
7. How do you center a div horizontally and vertically?
8. What is the difference between gap and margin?
9. What is flex-grow?
10. What is flex-shrink?
11. What is flex-basis?
12. What is the difference between Flexbox and Grid?

## Part 5 – CSS Grid

CSS Grid is a two-dimensional layout system.

It helps arrange elements in both rows and columns.

[The Ultimate Guide For Designing A Professional Responsive Website - DEV Community](https://images.openai.com/static-rsc-4/DDGZn3w-13BxnGYlZhayPbF6TBbyvch-JGhDsm1ILtsDbARMiX4IwjGamaRsJRn8cu-DnuQ_t12hRJ_KataZMxugV7qM5pLaHUHqXE4F6t15MsEauPo_brWVFb9gT6k-G15Kd6tlYmtEOONg6j4OP7t5cPgWf_bzzFaytXV1vKI?purpose=inline)

[dev.to](https://dev.to/mroman7/the-ultimate-guide-for-designing-a-professional-responsive-website-46ig?utm_source=chatgpt.com)

### Example: Create a three-column layout

```
<div class="grid-container">
    <div>Product 1</div>
    <div>Product 2</div>
    <div>Product 3</div>
    <div>Product 4</div>
    <div>Product 5</div>
    <div>Product 6</div>
</div>
```

```
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}
```

Explanation:

- `display: grid` enables Grid.
- `grid-template-columns` defines columns.
- `repeat(3, 1fr)` creates three equal columns.
- `gap` creates spacing between items.

### Important Grid properties

| Property                | Purpose                   |
| ----------------------- | ------------------------- |
| `display: grid`         | Enables Grid              |
| `grid-template-columns` | Defines columns           |
| `grid-template-rows`    | Defines rows              |
| `gap`                   | Defines spacing           |
| `grid-column`           | Controls column placement |
| `grid-row`              | Controls row placement    |
| `place-items`           | Aligns items on both axes |

### Flexbox vs Grid

| Flexbox                      | Grid                  |
| ---------------------------- | --------------------- |
| One-dimensional              | Two-dimensional       |
| Row or column                | Rows and columns      |
| Great for navigation         | Great for dashboards  |
| Good for component alignment | Good for page layouts |

Interview question: When would you use Flexbox and when would you use Grid?

Answer:

I use Flexbox when I need to arrange elements in one direction, such as a navigation bar. I use Grid when I need to create layouts with multiple rows and columns, such as an e-commerce product listing.

## Part 6 – CSS Positioning

CSS positioning determines where an element appears on a webpage.

There are five important position values.

[Where Am I? Understanding Position in CSS - DEV Community](https://images.openai.com/static-rsc-4/Pdh284oJiz5YMz-SbqdFMkrXz_-HsNRjvjhS44N9i37W80LRTCDZOcrqENXT5uDZJEzU3zJ4-VvKVdJJBfxb39KZvS4ZjEePENaH-Pp67mgn-_peZ_N6edysA5IXkbSV-nNBNitUFRk2gtn7mKYIxFiu0cJvkr7odqfEKqpOcrQ?purpose=inline)

[dev.to](https://dev.to/s_mathavi_2fa1e3ea8514f34/where-am-i-understanding-position-in-css-4209?utm_source=chatgpt.com)

### 1. Static

Default positioning.

```
.box {
    position: static;
}
```

### 2. Relative

The element is positioned relative to its normal position.

```
.box {
    position: relative;
    top: 20px;
    left: 30px;
}
```

### 3. Absolute

The element is positioned relative to its nearest positioned ancestor.

```
.parent {
    position: relative;
}

.child {
    position: absolute;
    top: 10px;
    right: 10px;
}
```

### 4. Fixed

The element stays in the same position relative to the viewport when scrolling.

```
.chat-button {
    position: fixed;
    bottom: 20px;
    right: 20px;
}
```

### 5. Sticky

The element behaves normally until it reaches a specified scroll position, then sticks.

```
.navbar {
    position: sticky;
    top: 0;
}
```

### Interview questions

1. What are the five CSS position values?
2. What is the difference between relative and absolute?
3. What is the difference between fixed and sticky?
4. What is the default position?
5. What is the purpose of top, bottom, left and right?
6. What is z-index?
7. What is stacking context?
8. How do you position an element at the bottom-right corner of a screen?
9. How do you create a sticky navbar?
10. What happens when an absolute element has no positioned ancestor?

## Part 7 – Responsive Web Design

Responsive web design means creating websites that adapt to different screen sizes.

For example:

[eCommerce UI: Top Tips to Boost Your Conversion Rates – GemPages](https://images.openai.com/static-rsc-4/hBWZgrTQp3p9LQKM9ZOFO18jfC5Z4NJRGY5EiykqDdKO2bBD5t--r0SU1J_hOJ28tv_S_4Y84b2s3_75ylHH-VMgP6rXC_FkpFtbEKBSj6q1Nl2DB3zFzoH1YCshmDirXkeRl4XlYoI_5XrHs0i23_h1BIPehQ20Rh6jUmcmh-g?purpose=inline)

Desktop

Multiple columns

[Nordcode Technology](https://images.openai.com/static-rsc-4/vcSbNAC04tAsQ0DNWuzJnmV5XuIJ1YGqaGhzqV2zZYnhihwxS2k1BNhM_kFfIHvhrX6mFNNk5l8W99ZimeKD90AccrTIkQjkJY2ENl7ZqbfQwvErPU3HjbMdhKKjubehH83-7pd1akdGWZr_oKNpw7h0ScAaV10Lbh2XNAlj8aQ?purpose=inline)

Tablet

Reduced columns

[Review Responsive Web Design](https://images.openai.com/static-rsc-4/abdbFWsRzfYJCKm58K6Cvniml_brWdh0DxDjt1Yx6qrhbXJMefrWTLuVHU6GkP9-Xc3bEWNFWa9DWwrqX-japT8FYeKXysBn_7m_pJbZbGaYpejpDUKJaSPSPYPCS-9xVitN1GfVo1CQk0ritW4jxfpadDXfPJAaJRpM0ZF3v_I?purpose=inline)

Mobile

Single column

### Why is responsive design important?

Because users access websites from:

- Desktop computers.
- Laptops.
- Tablets.
- Mobile phones.

### Important techniques

1. Flexible layouts.
2. Flexible images.
3. CSS media queries.
4. Relative units.
5. Flexbox.
6. CSS Grid.
7. Mobile-first development.

### Example

```
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

@media (max-width: 768px) {
    .container {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 480px) {
    .container {
        grid-template-columns: 1fr;
    }
}
```

This creates:

- Desktop: 3 columns.
- Tablet: 2 columns.
- Mobile: 1 column.

## Part 8 – CSS Media Queries

Media queries apply CSS rules based on screen characteristics.

Syntax:

```
@media (max-width: 768px) {
    .container {
        background-color: lightblue;
    }
}
```

### Common breakpoints

| Device category | Example breakpoint |
| --------------- | ------------------ |
| Mobile          | 480px              |
| Tablet          | 768px              |
| Laptop          | 1024px             |
| Desktop         | 1280px             |

These are common examples, not fixed standards.

### Mobile-first approach

Start designing for smaller screens and then add styles for larger screens.

```
.container {
    display: grid;
    grid-template-columns: 1fr;
}

@media (min-width: 768px) {
    .container {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (min-width: 1024px) {
    .container {
        grid-template-columns: repeat(3, 1fr);
    }
}
```

Interview questions

1. What is responsive web design?
2. What are media queries?
3. What is mobile-first design?
4. What is the difference between max-width and min-width?
5. What is the viewport?
6. Why do we use relative units?
7. How do you make images responsive?
8. How do you test responsive websites?
9. What is the difference between adaptive and responsive design?

## Part 9 – Tailwind CSS fundamentals

Tailwind CSS is a utility-first CSS framework.

Instead of writing separate CSS classes, you apply utility classes directly to HTML elements.

### Normal CSS approach

```
<button class="my-button">
    Login
</button>
```

```
.my-button {
    background-color: blue;
    color: white;
    padding: 10px 20px;
    border-radius: 8px;
}
```

### Tailwind CSS approach

```
<button class="bg-blue-500 text-white px-5 py-2 rounded-lg">
    Login
</button>
```

Both create a similar button.

### Important Tailwind classes

| Tailwind class   | Meaning              |
| ---------------- | -------------------- |
| `flex`           | display: flex        |
| `grid`           | display: grid        |
| `hidden`         | display: none        |
| `block`          | display: block       |
| `p-4`            | Padding              |
| `m-4`            | Margin               |
| `px-4`           | Horizontal padding   |
| `py-4`           | Vertical padding     |
| `text-center`    | Center text          |
| `font-bold`      | Bold font            |
| `bg-blue-500`    | Background color     |
| `rounded-lg`     | Rounded corners      |
| `shadow-lg`      | Large shadow         |
| `w-full`         | Width 100%           |
| `h-screen`       | Height 100vh         |
| `justify-center` | Center on main axis  |
| `items-center`   | Center on cross axis |
| `gap-4`          | Gap spacing          |

### Responsive classes in Tailwind

Tailwind uses responsive prefixes.

| Prefix | Meaning                          |
| ------ | -------------------------------- |
| `sm:`  | Small breakpoint and above       |
| `md:`  | Medium breakpoint and above      |
| `lg:`  | Large breakpoint and above       |
| `xl:`  | Extra-large breakpoint and above |
| `2xl:` | 2XL breakpoint and above         |

Example:

```
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
    <div class="bg-blue-100 p-4">Product 1</div>
    <div class="bg-blue-100 p-4">Product 2</div>
    <div class="bg-blue-100 p-4">Product 3</div>
</div>
```

This creates one column by default, two columns from the medium breakpoint, and three columns from the large breakpoint.

Interview questions

1. What is Tailwind CSS?
2. What is utility-first CSS?
3. What are the advantages of Tailwind CSS?
4. What is the difference between Tailwind and Bootstrap?
5. How do you apply responsive styles in Tailwind?
6. What is the purpose of `flex`?
7. What is the difference between `p-4` and `px-4`?
8. What is the purpose of `hover:`?
9. How do you create a responsive grid?
10. Can you customize Tailwind CSS?

# Part 10 – Hands-on practical exercise

Now let's combine everything you learned into one practical task.

Today's assignment

Create a responsive e-commerce product card for your ShopSphere project.

[Agenco](https://images.openai.com/static-rsc-4/jHyqGKMtJAIrz_P08NQ5d0q59iFO7Li9yiRB8IHnhGhnRLheUBkRAZ3h6Kuo5YNXAoMx3rY-sRIqFdi3e3BIHhwQQi9HcUdtB0WdKVrHpYvO_KjdorGWnT50Cb8amNfmTub2dLVUpujemMV-HdGgUTDqA_GlFbvdq0_NVri5LgQ?purpose=inline)

[agenco.io](https://agenco.io/?utm_source=chatgpt.com)

Your page should contain:

1. Product image.
2. Product name.
3. Product price.
4. Product description.
5. Add to Cart button.
6. Responsive layout.
7. Navigation bar.

Try this starter code:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">
    <title>ShopSphere</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="navbar">
        <h2>ShopSphere</h2>
        <nav>
            <a href="#">Home</a>
            <a href="#">Products</a>
            <a href="#">Cart</a>
        </nav>
    </header>

    <main class="container">
        <article class="product-card">
            <img src="https://placehold.co/300x200"
                 alt="Product image">

            <h2>Smart Watch</h2>
            <p>Premium smartwatch with modern features.</p>
            <h3>₹2,499</h3>

            <button>Add to Cart</button>
        </article>
    </main>

</body>
</html>
```

Create `style.css` and implement:

- Flexbox navigation.
- Centered product card.
- Box model properties.
- Rounded corners and shadows.
- Media query for mobile devices.

Try completing it yourself before checking tutorials.

# Part 11 – Test your understanding

Let's check whether you are ready for an interview.

HTML & CSS mini assessment

10/10 answered

Q1. What is the main difference between semantic and non-semantic HTML?

Semantic tags describe their purpose

Semantic tags are only used for styling

There is no difference

Semantic tags work only in HTML5

Correct

Semantic tags describe their meaning, such as header, nav, main and footer.

Q2. Which HTML element is used for the main content of a webpage?

section

main

footer

aside

Correct

The main element represents the dominant content of the document.

Q3. Which CSS property controls spacing inside an element's border?

margin

padding

outline

gap

Correct

Padding is the space between content and border.

Q4. Which display property enables Flexbox?

display: block

display: inline

display: flex

display: grid

Correct

display:flex establishes a flex formatting context.

Q5. Which CSS property aligns flex items along the cross axis?

justify-content

align-items

flex-direction

position

Correct

align-items controls alignment along the cross axis.

Q6. Which layout system is two-dimensional?

Flexbox

Inline

Grid

Float

Correct

CSS Grid handles both rows and columns.

Q7. Which position keeps an element fixed relative to the viewport?

relative

absolute

static

fixed

Incorrect – fixed

position:fixed keeps an element positioned relative to the viewport.

Q8. Which CSS feature is used for responsive layouts?

Variables

Media queries

Selectors only

Pseudo-elements

Correct

Media queries apply styles depending on viewport or device characteristics.

Q9. What does box-sizing:border-box do?

Removes padding

Includes padding and border in declared width

Adds margin

Removes border

Correct

The declared width includes content, padding and border.

Q10. What is Tailwind CSS?

A JavaScript library

A database

A utility-first CSS framework

A backend framework

Correct

Tailwind provides utility classes for styling directly in markup.

# Your score: 9/10

Try again

## What I want you to do now

Complete these three activities:

- Study the HTML and CSS concepts above.
- Build the ShopSphere product card.
- Complete the 10-question assessment.

After completing these, we'll move to a real technical interview practice session. I'll ask you HTML and CSS questions one by one, just like an interviewer, evaluate your answers, and teach you how to answer professionally.

Don't rush to Day 2. Make sure you can explain today's concepts in your own words.