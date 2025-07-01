# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

- See hover and focus states for all interactive elements on the page

### Screenshot

![](./screenshot.jpg)

### Links

- Live Site URL: [https://blog-preview-card-main-lake-nine.vercel.app/](https://blog-preview-card-main-lake-nine.vercel.app/)

## My process

### Built with

- HTML5
- [Tailwind CSS](https://tailwindcss.com/) - For styles

### What I learned

During this project, I deepened my understanding of **Tailwind CSS’s mobile-first responsive design**. I initially struggled with applying different `max-width` values for small and larger screens, mistakenly placing the responsive class prefixes in the wrong order. For example:

```html
<main class="sm:max-w-xs max-w-sm"></main>
```

resulted in unexpected layouts because Tailwind applies unprefixed classes to all screen sizes, and prefixed ones override styles from their breakpoint upward.

The correct approach is:

```html
<main class="max-w-xs sm:max-w-sm"></main>
```

which ensures `max-w-xs` applies to mobile/small screens and `max-w-sm` takes effect on screens wider than 640px.

For shadows, Tailwind’s default shadows didn’t work as i expected. I tried to research on how to apply them and landed on **Tailwind Shadow Generator** (resource added in Useful resources section below) to generate the shadow values, then applied them using Tailwind’s **arbitrary value syntax**:

```html
<main class="shadow-[10px_10px_0px_0px_#000000]"></main>
```

This approach gave me fine-grained control while staying within Tailwind’s utility-first framework.

### Useful resources

- [Tailwind Play CDN](https://tailwindcss.com/docs/installation/play-cdn) – This was my starting point for using Tailwind without setting up a full build process. It made it really easy to experiment and see results instantly, which was super helpful.

- [Tailwind Cheat Sheet – Nerdcave](https://nerdcave.com/tailwind-cheat-sheet) - This cheat sheet was incredibly useful for quickly looking up class names and syntax while working on the project. It's a great reference to have open alongside your code.

- [Tailwind Color Reference](https://tailwindcss.com/docs/colors) – This helped me understand and apply Tailwind’s color system correctly. I referred to it often while matching the design specs and choosing semantic, accessible colors.

- [Tailwind Shadow Generator](https://folge.me/tools/tailwind-shadow-generator) – This helped me generate custom shadow values quickly and visually, making it easier to craft shadows that fit the exact offsets, blur, and colors I needed for this design.

## Author

- Frontend Mentor - [@mubarakik](https://www.frontendmentor.io/profile/mubarakik)
- GitHub - [@mubarakik](https://github.com/mubarakik)
- LinkedIn - [@mubaraka-kikonyogo](https://www.linkedin.com/in/mubaraka-kikonyogo-950010271)
- X - [@mubarakik\_](https://twitter.com/mubarakik_)
