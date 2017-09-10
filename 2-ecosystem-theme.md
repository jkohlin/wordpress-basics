#Theme
A theme is a set of files with templates and functions controling how to present the content to the web. The main components of a theme are as follows:

- Templates and template parts
- PHP/Wordpress Functions
- Stylesheets and javascripts
- Static asset files
- Theme definition

## Templates and template parts

A template is like a blueprint, describing how the content will be presented on the frontend. The template contains HTML markup with placeholders for the content.

We can have a multiple set of templates, each with their own layout and functionality. When content is requested by a website visitor, Wordpress picks the correct template and renders it into an HTML-page.

In a theme we need at least one template which must be named `index.php`. This is a fallback template which will be responsible for rendering out content, if no other template is found.

Below is a simple example of the content of a theme's `index.php`:

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
                    // Previous/next post navigation.
                    twentyfourteen_paging_nav();
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

Just like with any PHP file we need to wrap all PHP-code inside `<?php` and `?>`. Everything outside these tags are regular HTML.

Starting from the top, we begin with a method called `get_header();`. This is a built in Wordpress method, which will include a **template part** into our current template. In this case a file named header.php will be found and embedded into our template. The content of this file contains html-header data aswell as body
