#Theme
A theme is a set of files with templates and functions controling how to present the content to the web. The main components of a theme are as follows:

- Templates and template parts
- PHP/Wordpress Functions
- Stylesheets and javascripts
- Static asset files
- Theme definition

## Templates and template parts

A Wordpress template is like a blueprint, describing how the content will be presented on the frontend. The template contains HTML markup with placeholders which will be filled with content from the database.

We can have a multiple set of templates, each with their own layout and functionality. When content is requested by a website visitor, Wordpress picks the correct template and renders it into a regular HTML-page.

In a theme we need at least one template which must be named `index.php`. This is a fallback template which will be responsible for rendering out content, if no other template is found.


