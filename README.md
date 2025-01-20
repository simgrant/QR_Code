# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)

## Overview

### Screenshot

<img width="1426" alt="Screenshot 2025-01-20 at 12 06 58 PM" src="https://github.com/user-attachments/assets/3d8a3513-5554-4a25-a62d-18e872765982" />

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

#### 1. **Using External Fonts with `@import`**
   - **Font Importing**: I learned how to import external fonts from Google Fonts using the `@import` rule in CSS. In this case, I imported the **Outfit** font, which is applied throughout the project. This allows me to enhance the typography of my web components without relying on system fonts.
   - Code: 
     ```css
     @import url('https://fonts.google.com/specimen/Outfit');
     ```

#### 2. **Working with Custom Properties (CSS Variables)**
   - **Global Variables for Colors**: I defined custom properties for color management using `:root`. This makes my styles easier to maintain and update since I only need to change the color values in one place.
   - Example:
     ```css
     :root {
         --primary-white: hsl(0, 0%, 100%);
         --primary-slate: hsl(212, 45%, 89%);
         --secondary-slate: hsl(216, 15%, 48%);
         --tertiary-slate: hsl(218, 44%, 22%);
     }
     ```
   - Using variables like `--primary-slate` for the background color and `--primary-white` for the card background keeps the color palette consistent throughout the component.

#### 3. **Responsive Web Design with Flexbox**
   - **Flexbox Layout**: I learned how to use **flexbox** for positioning and aligning elements, both horizontally and vertically. The layout is flexible and adapts to different screen sizes.
   - **Centering Elements**: By using `justify-content: center` and `align-items: center`, I can center content both horizontally and vertically, which is essential for this component.
   - Code:
     ```css
     .content {
         display: flex;
         justify-content: center;
         align-items: center;
         height: 100%;
     }
     ```

#### 4. **Building the Main View Component**
   - **Box Model & Flexbox Combination**: The main container (`.main-view`) is set to a fixed width and height, but it adjusts the positioning of child elements dynamically using flexbox. The container itself has a white background (`--primary-white`), and a border radius of `20px` for rounded corners.
   - Example:
     ```css
     .main-view {
         width: 260px;
         height: 400px;
         background-color: var(--primary-white);
         display: flex;
         justify-content: center;
         flex-direction: column;
         border-radius: 20px;
     }
     ```

#### 5. **Handling Images with `object-fit`**
   - **Responsive Image Handling**: I used the `object-fit: cover` property to ensure that the image inside the `.image-container` fills its container without distorting, while maintaining its aspect ratio.
   - Code:
     ```css
     img {
         width: 100%;
         height: 100%;
         object-fit: cover;
         border-radius: 10px;
     }
     ```
   - This property ensures that the QR code image will look good across different screen sizes.

#### 6. **Text Styling and Typography**
   - I worked on styling headings (`h1`) and paragraphs (`p`) inside the `.text` container. I used `font-weight` and `font-size` to control the appearance of text, ensuring that the font is easy to read and looks visually appealing.
   - Code Example:
     ```css
     .text h1 {
         font-size: 15px;
         font-weight: 700;
         text-align: center;
         color: var(--tertiary-slate);
         margin: 0 15px;
     }
     ```

#### 7. **Responsive Design with Media Queries**
   - I implemented a **media query** for screens between `375px` and `1440px` in width. This helps to adjust the body’s font size to ensure readability on various devices.
   - Code:
     ```css
     @media (min-width: 375px) and (max-width: 1440px) {
         body {
             font-size: 15px;
         }
     }
     ```
   - This allows the design to remain clean and readable on both smaller mobile devices and larger screens.


### Continued development

Going forward, I plan to continue practice with alignment and positioning using Flexbox, as well as incorportating Grid into future projects.


### Useful resources

- [Flexbox Froggy](https://flexboxfroggy.com/) - This helped me with learning how to position elements.
- [web.dev](https://web.dev/learn/css) - This is an amazing resource for learning CSS.

