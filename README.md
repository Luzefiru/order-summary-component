# Frontend Mentor - Order summary card solution

This is a solution to the [Order summary card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/order-summary-component-QlPmajDUj). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- See hover states for interactive elements

### Screenshot

![](./requirements/website-screenshot.png)

### Links

- Solution URL: [GitHub Repository](https://github.com/Luzefiru/order-summary-component)
- Live Site URL: [GitHub Pages Deployment](https://luzefiru.github.io/order-summary-component/)

## My process

### Built with

- [Tailwind CSS](https://tailwindcss.com/)
- Semantic HTML5 markup
- Flexbox
- Mobile-first workflow

### What I learned

This was an introductory project to let me acquaint myself with the Tailwind CSS workflow in styling rapid MVPs. I also started designing the component with a Mobile-first workflow which was easily done with Tailwind CSS.

I'd like to highlight my usage of Arbitrary Classes to manipulate a one-off style for a `box-shadow`:

```html
<div
  class="shadow-[0_16px_16px_-8px_rgba(118,108,241,0.3)] max-w-sm bg-white m-6 flex flex-col rounded-2xl overflow-hidden justify-center"
></div>
```

I also used the `rounded` utility class for `border-radius`, then `overflow-hidden` to hide any `<img>` elements that go beyond the `rounded` continer.

I was also practicing my usage of the `npx tailwindcss init` command to make the `tailwind.config.js` file so that I can add and `exports.theme.extend` my own design systems and `background-image` files.

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['./*.{html,ts,js}'],
  theme: {
    extend: {
      fontFamily: {
        sans: ['Red Hat Display', 'ui-sans-serif'],
      },
      colors: {
        primary: {
          'pale-blue': 'hsl(225, 100%, 94%)',
          'bright-blue': 'hsl(245, 75%, 52%)',
          'bluish-purple': '#5B48E6',
          'medium-slate-blue': '#766cf1',
        },
        neutral: {
          'very-pale-blue': 'hsl(225, 100%, 98%)',
          'desaturated-blue': 'hsl(224, 23%, 55%)',
          'dark-blue': 'hsl(223, 47%, 23%)',
        },
      },
      backgroundImage: {
        desktop: "url('/images/pattern-background-desktop.svg')",
        mobile: "url('/images/pattern-background-mobile.svg')",
      },
    },
  },
};
```

> I need to remember to remove any `.` relative paths when I use `url()` CSS functions and also to `@import` my `fontFamily` typefaces inside my `input.css` together with the `@tailwind` CSS directives.

### Continued development

I will keep practicing Tailwind CSS until I can match my Vanilla CSS coding speed and setup the development environment quickly without using any frameworks like React.

### Useful resources

- [Tailwind CSS Docs](https://tailwindcss.com/docs) - I had to search up some utility classes I'm not familiar with when I translate my intentions from Vanilla CSS to Tailwind CSS code. Some notable ones were `rounded`, `shadow`, `items-{direction}`, `justify-{direction}`, and `max-w-{size}`.

## Author

- Website - [Christian de Jesus IV](https://luzefiru.github.io/Portfolio/)
- Frontend Mentor - [@Luzefiru](https://www.frontendmentor.io/profile/Luzefiru)
