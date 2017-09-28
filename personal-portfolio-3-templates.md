## Assignment 3 - Templates

The wireframe sketches explains the website's different views, and how content is layed out on them. Before defining which templates we might need, a good start is to define the common parts of each template to instead create their building blocks.

### Bulding blocks
---
#### Header (header.php)
A common area used in all views with the logo, description and menu.

**Components used**
* Logo - Should be linked to the website's **home url** and show the **site title**
* Description - Should be linked and show the **site description**
* Menu - Should be using a **custom menu**
---
#### Post grid (partials/postgrid.php)
A list of posts losted in a grid with a taxonomy filter.

**Components used**
* Filter - Listing a taxonomy's terms to filter the grid items with JavaScript
* Post list - Looping all posts within a specific post type.
---
#### Content row (partials/content.php)
Presenting the content from a single post with image, text and taxonomy terms.

**Components used**
* Image - The current post's featured image.
* Title - The current post's title.
* Terms - The terms in a specific taxonomy, connected to the current post or all terms available in a specific taxonomy.
---
### Templates
