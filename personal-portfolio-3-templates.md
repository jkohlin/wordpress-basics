## Assignment 3 - Templates

The wireframe sketches explains the website's different views, and how content is layed out on them.

[Link to wireframe sketches]

### Bulding blocks
Before defining which templates we might need, a good start is to define the common parts of each template to instead create their building blocks. In Wordpress we can use template parts for this, and use them to build templates.

> Tip: Add static HTML for now where real content is missing. Come back later and change to outputing real content.

#### Navigation header (partials/navhead.php)
A common area used in all views with the logo, description and menu.

* Logo - Should be linked to the website's **home url** and show the **site title**.
* Description - Should be linked and show the **site description**.
* Menu - Should be showing a specific **custom menu**.

---
#### Post grid (partials/postgrid.php)
A list of posts losted in a grid with a taxonomy filter.

* Filter - Listing a taxonomy's terms to filter the grid items with JavaScript
* Post list - Looping all posts within a specific post type.
---
#### Content row (partials/content.php)
Presenting the content from a single post with image, text and taxonomy terms.

* Image - The current post's featured image.
* Title - The current post's title.
* Terms - The terms in a specific taxonomy, connected to the current post or all terms available in a specific taxonomy.
---

### Result
Create a minimum amount of templates using the template parts above, to match the content plan and wireframes. Each template must contain `get_header()` and `get_footer()`;

**Push your theme to the remote repository.**
