# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
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

![](./desktop.png) (./mobile.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- CSS Nesting
- Media Query
- Mobile-first workflow
- web responsive


### What I learned

When i use position: relative at the parent element (wrapper), the child element (wrapper-qr) that take in position: absolute can be offset (using property top, right, bottom and left) relative to the padding edge of the parent element. If no position property exist in the parent element, the child element will offset relative to the initial containing block of the viewport/HTML.
```html
<html>
  <body>
    <div class="wrapper">
      <div class="wrapper-qr">  </div>
    </div>
  </body>
</html>
```
```css
.wrapper {
  position: relative;
  width: 100vw;
  height: 100vh;
  background-color: hsl(289, 100%, 50%);
}

.wrapper-qr {
  background-color: hsl(289, 100%, 80%);

  position: absolute;
  top: 50%;
  left: 50%;

  transform: translate(-50%, -50%);
}
```

```css
.wrapper-qr {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50px, -50px);
}
```

The css property min-width define the width of an element that must be at least or greater than 375px, while max-width property simply means do not exceed 1440px

```css
min-width: 375px;
max-width: 1440px;
```

'em' unit apply to margin and padding scale relatively to it's parent font size.


## Author

- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/honlimwong)
