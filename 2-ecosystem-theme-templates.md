#Theme
A theme is a set of files with templates and functions controling how the content will be presentated on the frontend. These are the main components of a theme:

- Templates and template parts
- PHP/Wordpress Functions
- Stylesheets and javascripts
- Static asset files
- Theme definition

## Templates and template parts

Templates are used to render the content for presentation on the frontend. Technically the templates are PHP-files with HTML mixed with PHP-function calls.

When building a theme we are required to include a template called `index.php`. This will become the default template and be used to render all content.

In addition to `index.php` we as developers can add more templates to fit different content and situations. Wordpress will use the template filename to decide when to use which template.

> Note: Adding templates should be done with great care and not just to make small variantions of a layout. One template can present content i various ways with the help of PHP logic.

Below is an example of a theme's default template `index.php`:

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

In the middle of the document we find something called The Loop:

    if ( have_posts() ) :
        // Start the Loop.
        while ( have_posts() ) : the_post();
            get_template_part( 'content', get_post_format() );
        endwhile;
    else :
        // If no content, include the "No posts found" template.
        get_template_part( 'content', 'none' );
    endif;

The Wordpress loop is what we use to output content in our templates. A global variable called $wp_query will hold the current post's content and also provide helper methods to retrive that content.



### Template parts
In the example with `header.php` we were embedding something called a **template part**, which are smaller chunks of reusable template code. Much of our templates will be built by template parts together with HTML and Wordpress PHP-methods.

Below is the most common way of embedding template parts in a template:

	get_template_part( $slug, $name = null )
    
The two arguments are used to locate a specific filename inside our theme. To replicate what the method `get_header()` does, we can use `<?php get_template_part('header'); ?>`. Wordpress will only look in our theme's root directory, so if we had all our template parts in another folder (recommended) we would have to include that folder in the argument too: `<?php get_template_part('my-template-parts/header'); ?>`

The second argument can be used to look for other versions of the same template part. Let's say we had `header-simple.php` where some kind of alternation were made. We could then use  `<?php get_template_part('my-template-parts/header', 'simple'); ?>` to look for that template part first. If not found, Wordpress would instead look for `header.php` as a fallback. The file's naming is important here.
