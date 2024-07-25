# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![screenshot](./screenshot.jpeg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [https://ryan-ohanlon.github.io/nft-preview-card-component-main/](https://ryan-ohanlon.github.io/nft-preview-card-component-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

The primary challenge I had with this project was learning how to layer multiple images on top of each other and using the CSS :hover rule to layer a background color element and an image on top of the NFT image as well as making it a link.

While this wasn't an elequant solution, I was able to achieve the active state effect by creating two div elements. The first to contain both the img and div element and the second to act as a link and overlay for the background color for the :hover rule.

Using the flex rule set in the main element, the div element classified container could be set using the relative position and be given a set width to contain the image elements and the div element classified as overlay. The hover-img was positioned using the absolute rule and centered in the container by setting the top and left to 50% and setting the transform to -50%. Finally, the overlay was set using the position attribute with the absolute value and assigned the cyan hsl color with an opacity of 0 to not be seen. Then when the user hover's over the element, the opacity is set to .5 (50%) making it visible.


```html
    <div class="container">
      <img class="equilibrium" src="./images/image-equilibrium.jpg" alt="Equilibrium cube">
      <a href="#"><div class="overlay">
      </div>
      <img class="hover-img" src="./images/icon-view.svg" alt="eyeball icon"></a>
    </div>
```
```css
.container {
    position: relative;
    width: 100%;
    max-width: 320px;
}

.container:hover .hover-img {
    display: block; 
}

.hover-img {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    display: none;
}

.overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: .3s ease;
    background-color: hsla(178, 100%, 50%);
    border-radius: 1em;
}

.container:hover .overlay {
    opacity: .5;
  }
```

### Continued development

I would still like to continue developing my HTML framework skills. Having to layer multiple images and containers on top of each other and then adjust the CSS rules to make a hover effect shows how important designing the HTML framework is.

I'd also like to continue to develop structuring CSS rules an know when to assign classes to HTML elements and come up with a proper naming schema to make the code easier to read and understand.

### Useful resources

- [W3Schools](https://www.w3schools.com/howto/howto_css_image_overlay_icon.asp) - This helped find a solution on how to overlay an image and a background color above the NFT equilibrium image. Using two container elements and setting the link to be the container was the best solution I could find for this challenge.

## Author

- Website - [Ryan O'Hanlon](https://ryan-ohanlon.github.io/)
- Frontend Mentor - [@Ryan-OHanlon](https://www.frontendmentor.io/profile/Ryan-OHanlon)
- Twitter - [@RyanROHanlon](https://x.com/RyanROHanlon)