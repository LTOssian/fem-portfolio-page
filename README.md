# Frontend Mentor - Single-page design portfolio solution

This is a solution to the [Single-page design portfolio challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/singlepage-design-portfolio-2MMhyhfKVo).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Navigate the slider using either their mouse/trackpad or keyboard

### Screenshot

![](./assets/Capture%20web_14-9-2022_213656_127.0.0.1.jpeg)

### Links

- Solution URL: [My FEM Profile](https://your-solution-url.com)
- Live Site URL: [Github pages](https://ltossian.github.io/fem-portfolio-page/)

## My process

### Built with

- Semantic HTML5 markup
- Javascript
- CSS
- Flexbox
- CSS Grid
- Mobile-first workflow
- Vite

### What I learned

I learned how to use in practice JS classes, and I got a better understanding of grid layouts thanks to the skills section.

```css
#one {
  grid-area: 1 / 1 / span 2 / span 2;
}
#two {
  grid-area: 1;
}
#three {
  grid-area: 1;
}
#four {
  grid-area: 2 / 3 / 2 / span 2;
}
#five {
  grid-area: 1 / 5 / 1 / span 2;
}
#six {
  grid-area: 2 / 5 / 2 / span 2;
}
```
Building the class constructor was the most time consuming part. It was an important process since now I can use this class template for other projects. 

```js
constructor (element, options = {}) {
        this.element = element,
        this.options = Object.assign({}, {
            slidesToScroll: 1,
            slidesVisible: 1
        }, options)
        let children = [].slice.call(element.children);
        this.currentItem = 0;
        let root = this.createDivWithClass('carousel');
        let nextButton = document.querySelector('.carousel-right');
        let prevButton = document.querySelector('.carousel-left');
        this.translateX = 0;
        this.container = this.createDivWithClass('carousel__container');
        root.appendChild(this.container);
        this.element.appendChild(root);
        this.items = children.map((child) => {
            let item = this.createDivWithClass('carousel__item');
            item.appendChild(child);
            this.container.appendChild(item);
            return item
        })
       this.setStyle()
        nextButton.addEventListener('click', this.next.bind(this))
        prevButton.addEventListener('click', this.prev.bind(this))    
    }
}
```

### Continued development

In future projects I will focus on best practices for the mobile first workflow. This was my first time trying it and it was indeed faster and easier.


## Author

- Frontend Mentor - [@ltossian](https://www.frontendmentor.io/profile/ltossian)
- Twitter - [@louisantch](https://www.twitter.com/louisantch)


## Acknowledgments

Kevin Powell's CSS videos helped a lot for the grid layout !
