# Frontend Mentor - Newsletter sign-up form with success message solution

This is a solution to the [Newsletter sign-up form with success message challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/newsletter-signup-form-with-success-message-3FC1AZbNrv). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 


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


## Overview

### The challenge

Users should be able to:

- Add their email and submit the form
- See a success message with their email after successfully submitting the form
- See form validation messages if:
  - The field is left empty
  - The email address is not formatted correctly
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page


### Screenshot

![](./solution-screenshot.jpg)


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)


## My process

### Built with
- Semantic HTML5 markup
- CSS custom properties
- CSS variables
- CSS Grid
- BEM methodology
- Mobile-first workflow


### What I learned
In this project, I tried again to use grid areas to make responsive layout. I don't know if it was the best solution, maybe I just made things harder for myself, but in any case I got more experience with this grid feature.


```css
.newsletter-page {
    display: grid;
    grid-template-columns: var(--side-padding) 1fr var(--side-padding);
    grid-template-areas:
    "pic pic pic"
    "... content ...";
}


@media (min-width: 500px) {
  .newsletter-page {
      grid-template-columns: 2rem 1fr 2rem 1fr 2rem;
      grid-template-areas: 
      "... content ... pic ...";

      align-items: center;
      padding-block: 1rem;
  }
}
```


When it comes to javascript, it was my first custom form validation i made. I learned how to prevent the default behaivor of some events such as "submit" with help of .preventDefault(). For email validation, I used regular expressions to make sure the user input matched a certain pattern. 

Near the end of the development i learned about the trim function which removes any space before and after a string. A useful feature that I haven't heard of for some reason.

```js
// Regular expressions 
const emailRegext = new RegExp(/^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$/);
if (emailRegext.test(emailInputValue) === false) { /* code */ }


// prevent default 
form.addEventListener("submit", (event) => {
    event.preventDefault()

    validateEmailInput()
});
```


### Continued development
I partly managed to make the layout responsive. However the typography is not so fluid yet. It is one of my weak points I need to work on. 


### Useful resources
- [Example resource 1](https://youtu.be/In0nB0ABaUk?feature=shared) - Got to know about .preventDefault function


## Author
- Frontend Mentor - [@DaniilGurski](https://www.frontendmentor.io/profile/DaniilGurski)
