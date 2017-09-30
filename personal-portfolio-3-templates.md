## Assignment 3 - Templates
Look at the wireframe sketches explains the website's different views, and how content is layed out on them.

[Wireframe sketches](documents/portfolio-theme.pdf)

### Bulding blocks
A good start is to define and create the common parts of the template. By doing so we can build all templates we need effectively and without repeating any code. Wordpress' template parts is perfect for this. It's important to use general naming describing the parts' appearence and behavior, instead of the exact context we might use them for now.

#### Header navigation
<img src="https://github.com/farkost/wordpress-basics/blob/gh-pages/images/header.png" width="300">
`partials/navhead.php`
A common area used in all views with the logo, description and menu.

* Logo - Should be linked to the website's **home url** and show the **site title**.
* Description - Should be linked and show the **site description**.
* Menu - Should be showing a specific **custom menu**.

#### Postgrid
<img src="https://github.com/farkost/wordpress-basics/blob/gh-pages/images/postgrid.png" width="300">
`partials/postgrid.php`
A collection of posts listed in a grid with a taxonomy filter.

* Filter - Listing a taxonomy's terms to filter the grid items with querystring parameters.
* Post list - Looping all posts within a specific post type and the current querystring value.

#### Breadcrumbs
<img src="https://github.com/farkost/wordpress-basics/blob/gh-pages/images/breadcrumbs.png" width="300">
`partials/breadcrumbs.php`
Showing the current post's location in hierarchy.

#### Text content
<img src="https://github.com/farkost/wordpress-basics/blob/gh-pages/images/textcontent.png" width="300">
`partials/content.php`
Presenting the content from a single post with title, text and taxonomy terms.

* Title - The current post's title.
* Content - The current post's content.
* Terms - The terms in a specific taxonomy, connected to the current post or all terms available in a specific taxonomy.

> Tip: Use a conditional statement to check if the template part us beeing used with a single project or not. Can be useful when listing different collection of the taxonomy terms.

### Result
Create a minimum amount of templates using the template parts above, to match the content plan and wireframes. Each template should begin with `get_header()` and end with `get_footer()`;

**Push your theme to the remote repository.**

> Tip: If you need help, use Google or Wordpress Offical Codex: https://codex.wordpress.org/. If stuck please visit the Slack channel and ask for help.
