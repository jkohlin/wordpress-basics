#Theme
A theme is a set of files with templates and functions controling how the content will be presentated on the frontend. These are the main components of a theme:

- Templates and template parts
- PHP/Wordpress Functions
- Stylesheets and javascripts
- Static asset files
- Theme definition

## Templates and template parts

Templates are used to structure the content for presentation on the frontend. Technically the templates are PHP-files with HTML and PHP-function calls.

When building a theme we are required to include a template called `index.php`. This will become the default template and be used for all post types.

> Note: Adding more templates should be done with care and only when in need of a dramatic change of layout. Smaller layout variations depending on the current content can easily be made within the same template.

Below is a basic example of a theme's default template `index.php`:

    <?php

    get_header(); ?>

    <div id="main-content" class="main-content">

        <div id="primary" class="content-area">
            <div id="content" class="site-content" role="main">

            <?php
                if ( have_posts() ) :
                    // Start the Loop.
                    while ( have_posts() ) : the_post();
                        get_template_part( 'content', get_post_format() );
                    endwhile;
                else :
                    // If no content, include the "No posts found" template.
                    get_template_part( 'content', 'none' );
                endif;
            ?>

            </div><!-- #content -->
        </div><!-- #primary -->
        <?php get_sidebar( 'content' ); ?>
    </div><!-- #main-content -->

    <?php
    get_sidebar();
    get_footer();

What we see here is PHP and HTML mixed in one PHP-file. In the middle of the document we find something called The Loop:

    if ( have_posts() ) :
        // Start the Loop.
        while ( have_posts() ) : the_post();
            get_template_part( 'content', get_post_format() );
        endwhile;
    else :
        // If no content, include the "No posts found" template.
        get_template_part( 'content', 'none' );
    endif;

Here is where posts are retrieved from the database. The methods `have_posts()` and `the_post()` both are members of an object called $wp_query. It's an instance of the class `WP_Query`and is available in all our templates.

### Template parts
In the example with `header.php` we were embedding something called a **template part**, which are smaller chunks of reusable template code. Much of our templates will be built by template parts together with HTML and Wordpress PHP-methods.

Below is the most common way of embedding template parts in a template:

	get_template_part( $slug, $name = null )
    
The two arguments are used to locate a specific filename inside our theme. To replicate what the method `get_header()` does, we can use `<?php get_template_part('header'); ?>`. Wordpress will only look in our theme's root directory, so if we had all our template parts in another folder (recommended) we would have to include that folder in the argument too: `<?php get_template_part('my-template-parts/header'); ?>`

The second argument can be used to look for other versions of the same template part. Let's say we had `header-simple.php` where some kind of alternation were made. We could then use  `<?php get_template_part('my-template-parts/header', 'simple'); ?>` to look for that template part first. If not found, Wordpress would instead look for `header.php` as a fallback. The file's naming is important here.