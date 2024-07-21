# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### Screenshot

![](assets/images/recipe-page.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- BEM
- Logical Properties
- Custom Properties

### What I learned

With this challenge I learned a lot of things:

- Proper use of `<b>` or `span` instead that`<strong>`;
- [New HTML tags](#table) that I never used before `<table>`\, `<tr>`\  ,`<td>`;
- [How to style `<table>` and his elements](#table);
- The `:last-child` pseudo-class;
- The `::marker` pseudo-element and how to work with it;
- [How to create a custom `::marker` for `<ul>` and `<ol>`](#custom-marker-and-counter-function);
- [How to work with `counter()` function](#custom-marker-and-counter-function).

##### Table
```html
<table>
  <tr class="d-grid">
    <td>Calories</td>
    <td class="accent"><b>277kcal</b></td>
  </tr>
</table>
```
```css
/* Style for nutrition table */
table {
    border-collapse: collapse;
}

tr  {
    grid-template-columns: 1fr 1fr;
    gap: var(--primitive-m-16);
    border-block-end: 1px solid var(--clr-divider);
}

td {
    padding-inline: var(--primitive-p-32) 0;
    padding-block: var(--primitive-p-12);
}

td:last-child {
    padding-inline: 0 var(--primitive-p-32);
}
```
##### Custom marker and counter function
```html
<ul class="card-recipe__list d-grid">
  <li class="card-recipe__list-item bullett">2-3 large eggs</li>
</ul>

<ol class="card-recipe__list d-grid">
  <li class="card-recipe__list-item numered"><span><b>Beat the eggs:</b>
    In a bowl, beat the eggs with a pinch of salt and pepper until they are well mixed.
    You can add a tablespoon of water or milk for a fluffier texture.</span>
  </li>
</ol>
```
```css
/* ul and ol style */
.card-recipe__list {
    gap: var(--primitive-m-8);
    padding: 0;
}

/* Set marker position inside to ol */
.card-recipe__section > ol {
    list-style-position: inside;
    counter-reset: list-num;
}

/* General style for li items */
.card-recipe__list-item {
    display: flex;
    gap: var(--primitive-m-28);
}

/* Align bullett points vertically
   center with the text inside li
*/
.bullett {
    align-items: center;
}

/* Define bullett points for ul li */
.bullett::before {
    position: relative;
    content: '\2022';
    left: var(--primitive-m-8);
    font-size: 1.5rem;
    color: var(--clr-cardSectionHeading);
}

/* Bulletts modifier to set the color
   to the bulletts of card banner*/
.bullett--info::before {
    color: var(--clr-cardInfoHeading);
}

/* Define number points for ol li */
.numered::before {
    position: relative;
    counter-increment: list-num;
    content: counter(list-num) ". ";
    left: var(--primitive-m-8);
    font-weight: var(--fw-bold);
    color: var(--clr-cardSectionHeading);
}
```

### Continued development

Within next challenge I want to continue focusing on **CSS Grid**, reinforce my knwoledge with the elements that I learned in this challenge, both side, **CSS** and **HTML** and even start to use some **JavsScript**.

### Useful resources

- [How to use :last-child selector](https://developer.mozilla.org/en-US/docs/Web/CSS/:last-child) - I found this link usefull because I know the concept of that selector, but I never work with it and I didn't know the syntax.

- [Getting started with <table>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table) - As mentioned before there is some **HTML** tag that I never use before, I use thi article to start with it.

- [More Docs on <table> and his childs](https://www.w3schools.com/html/html_tables.asp) - Just another reference to build a nice table.

- [Use <b> or <span> instead of <strong>](https://html.com/tags/strong/) - This article was help me to understand wich **HTML** tags was more appropriately to **bold** text.

- [How to create a custom marker for a list](https://stackoverflow.com/questions/78394172/centering-vertically-multiple-line-list-element-to-the-dot) -

- [More on how to create custom marker](https://idkshite.com/posts/vertical-center-bullet) - I didn't use this method but I tried it and I think in other scenarios it could be usefull.

- [Why we need a custom marker](https://stackoverflow.com/questions/71911768/css-list-marker-not-inline-with-text) -

- [](https://www.example.com) -

- [](https://www.example.com) -

- [](https://www.example.com) -

- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
