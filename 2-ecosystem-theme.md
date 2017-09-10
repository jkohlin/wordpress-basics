# Templates and template parts

A Wordpress template is like a blueprint, describing how the content will be presented on the frontend. A template contains HTML markup, along with placeholders for the content.

We can have a multiple set of templates, each with their own layout and functionality. When content is requested by a website visitor, Wordpress picks the correct template and renders it into a regular HTML-page.

Templates, which are PHP-files utilizing Wordpress' built in methods, must be named properly for the template system to know which template to pick.

####The default template
For a theme to work, we need at least one template. This required base template must be named index.php.
