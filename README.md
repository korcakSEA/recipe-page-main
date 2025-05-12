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

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### Screenshot

![](![alt text](image.png))

![](![alt text](image-1.png))

### Links

- Solution URL: https://github.com/korcakSEA/recipe-page-main.git
- Live Site URL: https://korcaksea.github.io/recipe-page-main/

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties


### What I learned

In this challenge I learned a lot of new stuffs about CSS. Especially usage of min(), max() and clamp() functions.

Of course, this challenge can be done with using Flex layout, Grid or media query, but I personally preferred not using them.
The thing I found it difficult is making page, border-radius, padding, and margin properties responsive.

The other important thing I learned during this project is called nested or scoped styling. So it helps to improve readability, maintainability, and modularity of styles. 

```css
ol,ul{
    padding-left: var(--space-300);

    li{
        padding-left: var(--space-150);
        margin-bottom: var(--space-150);
        line-height: 1.5;
        
    }

    li::marker{
        color: var(--Rose-800);
        font-weight: var(--font-weight-semibold);
    }
    
}
```

And as always image styling. At the beginning I CSS properties on image to add padding and border radius. Unfortunately, they do not go well together.

So as said in the comments: "Set the padding on "wrap" not on the image (setting paddings on images does not make much sense :)), that should fix your problem."

You can also find example of min(), max() functions usage, see below:

```html
  <div class="image-container">
    <img class="card-image" src="/recipe-page-main/assets/images/image-omelette.jpeg" alt="omelette photo">
  </div>
```
```css
.image-container{
    margin-bottom: 0;
    /* Responsive padding */
    padding-inline:max(0rem,min(2rem, 50vw - var(--max-width) / 2));
    padding-top: max(0rem,min(2rem, 50vw - var(--max-width) / 2));
}

.card-image{

    /* Responsive border-radius from 0px to 12px */
    /* border-radius: clamp(0px, calc((100vw - 375px) / 20), 12px); */

    border-radius:max(0rem,min(12px, 50vw - var(--max-width) / 2));

    /* border-radius: var(--border-radius-100); */
}
```


### Continued development

In the future, when I will be good at responsive design i will take a look at this project one again :D.

### Useful resources

- [Example resource 1](https://stackoverflow.com/questions/9409632/border-radius-and-padding-not-playing-nice) - This helped me for Border-radius and padding issue.

- [Example resource 2](https://web.dev/articles/min-max-clamp) - This is an amazing article which helped me finally understand CSS min(), max(), and clamp(). I'd recommend it to anyone still learning this concept.

## Author

- Frontend Mentor - [@korcakSEA](https://www.frontendmentor.io/profile/korcakSEA)


