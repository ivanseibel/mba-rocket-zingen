
# Zingen Karaoke - Responsive Design Study Project

## Overview

Zingen Karaoke is a study project aimed at reviewing and applying concepts of responsive design and mobile-first principles. The project includes an HTML file (`index.html`) and several CSS files that style various components of the webpage. The goal is to create a seamless and responsive karaoke web app that works well across different devices and screen sizes.

## Project Structure

The project consists of the following files:

- `index.html`: The main HTML file containing the structure of the webpage.
- CSS Files:
  - `about.css`: Styles for the About section.
  - `buttons.css`: Styles for various buttons.
  - `cards.css`: Styles for the card components.
  - `download.css`: Styles for the Download section.
  - `features.css`: Styles for the Features section.
  - `footer.css`: Styles for the Footer.
  - `global.css`: Global styles and variables.
  - `header.css`: Styles for the Header.
  - `hero.css`: Styles for the Hero section.
  - `index.css`: The main CSS file that imports other CSS files.
  - `pricing.css`: Styles for the Pricing section.
  - `sections.css`: Styles for general sections.
  - `social.css`: Styles for social media icons.
  - `utility.css`: Utility classes for common styles.

## Key Concepts

### Responsive Design

Responsive design is about creating web pages that look good on all devices. The project uses media queries to apply different styles based on the screen size. For example:

- **Mobile First**: The base styles are designed for mobile devices first. Media queries are used to enhance the design for larger screens.
- **Media Queries**: Various CSS files use media queries to adjust styles for screens larger than 80em (1280px) and smaller screens.

### Mobile First Approach

The mobile-first approach ensures that the website is optimized for mobile devices before adding styles for larger screens. This is evident in the use of media queries that progressively enhance the design:

```css
@media (width >= 80em) {
  .container {
    --max-width: 80rem;
  }
  
  .desktop-only {
    display: initial;
  }  
  
  .even-columns {
    grid-auto-flow: column;
    grid-auto-columns: 1fr;
  }
}

@media (width < 80em) {
  .desktop-only {
    display: none;
  }
}
```

### CSS Grid and Flexbox

The project extensively uses CSS Grid and Flexbox for layout management, ensuring flexible and responsive designs:

- **CSS Grid**: Used for creating complex layouts, especially for the card components and section layouts.
- **Flexbox**: Used for aligning items within containers, such as in navigation and button groups.

## File Details

### `index.html`

The main HTML file includes the structure for various sections such as the header, hero, features, pricing, and footer. It links to the `index.css` for styling.

### `index.css`

This file imports all other CSS files to modularize the styles and maintain a clean structure:

```css
@import url(global.css);
@import url(utility.css);
@import url(buttons.css);
@import url(social.css);
@import url(header.css);
@import url(hero.css);
@import url(sections.css);
@import url(about.css);
@import url(cards.css);
@import url(features.css) (width >= 80em);
@import url(pricing.css);
@import url(download.css);
@import url(footer.css);
```

### Individual CSS Files

Each CSS file focuses on styling a specific part of the webpage:

- **Global Styles (`global.css`)**: Contains variables and global resets.
- **Utility Styles (`utility.css`)**: Includes utility classes for padding, margins, and other common styles.
- **Component Styles**:
  - `header.css`: Styles for the navigation header.
  - `hero.css`: Styles for the hero section, including background images and text alignment.
  - `features.css`: Styles for the features section, using grid layout for cards.
  - `pricing.css`: Styles for the pricing section, including card layouts and pricing details.
  - `footer.css`: Styles for the footer, including social media icons and links.
  - `about.css`, `download.css`, `sections.css`: Styles for the respective sections.

## Live Demo

You can view the live demo of the Zingen Karaoke project [here](https://ivanseibel.github.io/mba-rocket-zingen/).

## Conclusion

This project is an excellent example of applying responsive design and mobile-first principles in a real-world scenario. By modularizing the CSS and using advanced layout techniques like CSS Grid and Flexbox, the project achieves a highly responsive and user-friendly design.

Feel free to explore the code and experiment with different styles and layouts to deepen your understanding of responsive design!
