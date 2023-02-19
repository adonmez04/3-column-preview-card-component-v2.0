# Frontend Mentor - 3-column-preview-card-component-v2.0

**Table of Contents**

- [Frontend Mentor - 3-column-preview-card-component-v2.0](#frontend-mentor---3-column-preview-card-component-v20)
  - [Welcome! 👋](#welcome-)
  - [Links](#links)
  - [Overview](#overview)
  - [The Problems and Solutions](#the-problems-and-solutions)
  - [Useful Resources](#useful-resources)
  - [Acknowledgments](#acknowledgments)
  - [Author](#author)

## Welcome! 👋

Welcome to my solution page. I hope you'll find some good implemantions for this project here.

![3-column-preview-card-component-v2.0 ](./design/desktop-preview.jpg)

## Links

- [My Live Site](https://adonmez04.github.io/3-column-preview-card-component-v2.0/)

- [My Solution Page](https://www.frontendmentor.io/solutions/3columnpreviewcardcomponentv20-pNYXxIs5Y4)

- [The Challenge Page](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-)

## Overview

This is my second solution to the project (the mobile first again). I got a huge feedback from Grace Snow and fixed some bugs according to them. I tried to solve some problems with responsive design. I guess this solution is a progress. I know there are lots of issues still here. I hope I can find and fix them.

I couldn't understand how to fix component size without width and height properties. Thanks to Grace, she wrote a huge comment all about this, `You will need to add more margin-top / bottom to increase the space between buttons and paragraphs once the heights have been removed.` and I got it. I should use margin and padding to set the component area. I was avoiding using margin because margin-collapse. But if I want to give some area to the item, I can use margin and padding. This will also be responsive.

## The Problems and Solutions

In this project, there is a hierarchy problem. The preview-card areas are the iteration items and all iteration items should have the same property and structure. However, the page must have at least one h1 tag. It's a clear problem that I couldn't solve. However thanks to Dave Quah's feedback, I have a solution right now.

**1 - From Dave Quah:**

I think one thing that could be improved on is the heading levels. I'd view "Sedans", "SUVs" and "Luxury" as the same heading, but I also understand that we do not want multiple `<h1>`.

I think it would be better to declare a `<h1>` but set it for screen readers only (meaning not visible but screen reader would still pick it up), and keep "Sedans" as a `<h2>` with "SUVs" and "Luxury". E.g.

// CSS

```css
.sr-only {
  position: absolute;
  top: auto;
  height: 1px;
  width: 1px;
  overflow: hidden;
  clip: rect(1px, 1px, 1px, 1px);
  white-space: nowrap;
}
```

// HTML

```html
<h1 class="sr-only">Learn more about our cars</h1>
...
<h2>Sedans</h2>
<h2>SUVs</h2>
<h2>Luxury</h2>
```

Another suggestion is that for images that are decorative, the alt should be alt="" instead of alt="#", or alternatively you could also set aria-hidden="true" to hide it from screen readers.

<!-- ## My Questions for The Community -->

<!-- ## Community Feedbacks -->

<!-- ## Good Implementations -->

## Useful Resources

- [About heading levels by Kevin Powell](https://www.youtube.com/watch?v=NexL5_Vdoq8)

- [Decorative images](https://www.w3.org/WAI/tutorials/images/decorative/)

- [aria-hidden](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-hidden)

## Acknowledgments

- Thanks Grace Snow for your helpful comment. [@grace-snow](https://www.frontendmentor.io/profile/grace-snow)

- Thanks Dave Quah for your helpful comment. [@Milleus](https://www.frontendmentor.io/profile/Milleus)

## Author

- My Frontend Mentor Profile Page - [@adonmez04](https://www.frontendmentor.io/profile/adonmez04)
- For those of you reading this, have a nice day!
