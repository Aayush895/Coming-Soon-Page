# Frontend Mentor - Base Apparel coming soon page solution

This is a solution to the [Base Apparel coming soon page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/base-apparel-coming-soon-page-5d46b47f8db8a7063f9331a0). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Receive an error message when the `form` is submitted if:
  - The `input` field is empty
  - The email address is not formatted correctly

### Screenshot

![Desktop](/Screenshots/desktop.png)

### Links

- Solution URL: [Github Link](https://github.com/Aayush895/Coming-Soon-Page)
- Live Site URL: [Deployed Link](https://coming-soon-email-validation.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Javascript
- Mobile Simulator chrome extension for checking the responsiveness of the website on various devices

### What I learned

From this project, I learned about how to create a basic form validation along with the logic to create the form validation. Below is the javascript code snippet that contains the logic for form validation:

```js
function validateEmail(email) {
  const atSign = email.indexOf('@')
  const dotSign = email.indexOf('.')
  if (atSign < 1 || dotSign < atSign + 2 || dotSign + 2 >= email.length) {
    document.querySelector(
      '.validity-message'
    ).innerText = `Invalid email, please try again!`
    document.querySelector('.validity-message').classList.remove('success')
    document.querySelector('.validity-message').classList.add('error')
  } else {
    document.querySelector(
      '.validity-message'
    ).innerText = `Form Submission Successful!`
    document.querySelector('.validity-message').classList.remove('error')
    document.querySelector('.validity-message').classList.add('success')
  }

  setTimeout(() => {
    document.querySelector('.validity-message').innerText = ''
  }, 2000)

  input.value = ''
}
```

### Continued development

Now that I know how to create a basic form validation, I want to use this acquired knowledge to experiment and create more advanced form validaiton pages in the coming projects that have a need for it.

### Useful resources

- [Form Validation](https://www.scaler.com/topics/email-validation-in-javascript/) - This article helped me greatly to enhance my understanding about form validation.


## Author

- Frontend Mentor - [@Aayush895](https://www.frontendmentor.io/profile/Aayush895)
- Twitter - [@JhaAayush895](https://www.twitter.com/JhaAayush895)


## Acknowledgments

I would like to thank the entire frontend-mentor team for providing such interesting challenges to test and improve my skills in the domain of frontend web development.
