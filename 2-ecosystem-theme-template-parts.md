## Template parts
When making templates we have to prevent duplicate code, as it will become hard to maintain. By wrapping common chunks into components (PHP-files) we can reduce the amount of code and simplify maintenance.

Much of our templates will be built by template parts and this is how a template part is included:

	get_template_part( $slug, $name = null )
    
The two arguments are used to locate a specific filename inside our theme's folder. Wordpress will  look for the file in the theme's root directory, but if we had all our template parts in another folder (recommended) we would have to include that folder in the argument. Like so: `<?php get_template_part('my-template-parts/header'); ?>`

The second argument can be used to look for other versions of the same template part. Let's say we had `header-simple.php` where some kind of alternation were made. We could then use  `<?php get_template_part('my-template-parts/header', 'simple'); ?>` to look for that template part first. If not found, Wordpress would instead look for `header.php` as a fallback. The file's naming is important here.

Something all template needs are HTML-markup like <body> and <head> with imports and scripts. Coding all this in each template would be stupid, so we can instead create template parts called `header.php` and `footer.php` and include them in all our templates. These two example is so common that Wordpress gives us shorthand methods for including them; `get_header()` and `get_footer()`. These can be seen in all templates' top and bottom.
