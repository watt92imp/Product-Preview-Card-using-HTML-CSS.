# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![Desktop-Preview](./screenshot_desktop_preview.jpg)
![Mobile-Preview](./screenshot_mobile_preview.jpg)

### Links

- Solution URL: [Add solution URL here](https://www.frontendmentor.io/solutions/responsive-card-component-using-cssandhtml-08-NzbUceA)
- Live Site URL: [Add live site URL here](https://watt92imp.github.io/Product-Preview-Card-using-HTML-CSS./)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```html
<main>
      <div class="card">
        <picture class="preview">
          <source
            media="(min-width:641px)"
            srcset="./images/image-product-desktop.jpg"
          />
          <source
            media="(max-width:641px)"
            srcset="./images/image-product-mobile.jpg"
          />
          <img
            src="./images/image-product-desktop.jpg"
            alt="A floral, solar and voluptuous interpretation composed by Olivier
          Polge, Perfumer-Creator for the House of CHANEL."
          />
        </picture>
        <div class="content">
          <span class="product-title">Perfume</span>
          <h1 class="title">Gabrielle Essence Eau De Parfum</h1>
          <p class="info">
            A floral, solar and voluptuous interpretation composed by Olivier
            Polge, Perfumer-Creator for the House of CHANEL.
          </p>
          <div class="price">
            <h2>$149.99</h2>
            <del>$169.99</del>
          </div>
          <button class="btn">
            <img src="./images/icon-cart.svg" alt="" class="icon-cart" />Add to
            Cart
          </button>
        </div>
      </div>
    </main>
```

```css
@import url("https://fonts.googleapis.com/css2?family=Fraunces:wght@700&family=Montserrat:wght@500;700&display=swap");
:root {
  --Dark-cyan: hsl(158, 36%, 37%);
  --Cream: hsl(30, 38%, 92%);
  --Very-dark-blue: hsl(212, 21%, 14%);
  --Dark-grayish-blue: hsl(228, 12%, 48%);
  --White: hsl(0, 0%, 100%);
}
* {
  margin: 0;
  padding: 0;
}
body {
  display: flex;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  background-color: var(--Cream);
}
.card {
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2);
  background-color: var(--White);
  display: flex;
  border-radius: 0.5rem;
  width: 600px;
}
.preview {
  width: 300px;
  height: auto;
  position: relative;
  border-radius: 0.5rem 0 0 0.5rem;
}
.preview img {
  width: auto;
  width: 300px;
  min-height: 100%;
  border-radius: 0.5rem 0 0 0.5rem;
}
.content {
  width: auto;
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  font-family: "Montserrat", sans-serif;
}
.content .title {
  font-family: "Fraunces", serif;
  font-weight: 700;
}
.product-title {
  text-transform: uppercase;
  letter-spacing: 5px;
  font-size: 500;
  font-size: 12px;
  color: var(--Dark-grayish-blue);
}
.info {
  color: var(--Dark-grayish-blue);
  font-size: 15px;
  font-weight: 500;
  line-height: 1.6;
}
.price {
  width: 150px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.price h2 {
  font-size: 32px;
  font-family: "Fraunces", serif;
  color: var(--Dark-cyan);
}
.price del {
  text-decoration: line-through;
  color: var(--Dark-grayish-blue);
  font-size: 14px;
  margin-left: 1.5rem;
}
.btn {
  width: 100%;
  background-color: var(--Dark-cyan);
  padding: 15px;
  border: none;
  color: var(--White);
  font-size: 16px;
  font-weight: 700;
  border-radius: 0.5rem;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  column-gap: 0.5rem;
}
.btn:hover {
  background-color: var(--Very-dark-blue);
}

@media screen and (max-width: 641px) {
  .card {
    flex-direction: column;
    max-width: 375px;
    width: 100%;
    justify-content: center;
  }
  .content {
    width: 100%;
    max-width: 325px;
    height: auto;
    gap: 1rem;
  }
  .preview {
    width: 100%;
  }
  .preview img {
    width: 100%;
    border-radius: 0.5rem 0.5rem 0 0;
  }
  .btn {
    max-width: 375px;
    width: 100%;
  }
}

```
