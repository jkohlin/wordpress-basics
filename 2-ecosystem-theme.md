#Theme
A theme is a set of files with templates and functions controling how to present the content to the web. The main components of a theme are as follows:

- Templates and template parts
- PHP/Wordpress Functions
- Stylesheets and javascripts
- Static asset files
- Theme definition

## Templates and template parts

A template is like a blueprint, describing how content will be presented on the frontend. The template contains HTML markup with placeholders for the content.

We can have a multiple set of templates, each with their own layout and functionality. When content is requested by a website visitor, Wordpress picks the correct template and renders it into an HTML-page.

In a theme we need at least one template which must be named `index.php`. This is a fallback template which will be responsible for rendering out content, if no other template is found.

Below is a basic example of a theme's default template:

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

Starting from the top, we begin with a method called `<?php get_header(); ?>`. This is a built in Wordpress method which will look in our theme for a file called `header.php` and embed it's content into our template's top. Inside `header.php` we will find code that applies to all templates, should we have more than one. Making changes to header.php would then automatically apply to all our templates, and we wouldnt have to do repetative tasks. **The art of not repeating ourself is very important when creating themes.**

### Template parts
In the example with `header.php` we were embedding something called a **template part**, which are smaller chunks of reusable template code. Much of our templates will be built by template parts together with HTML and Wordpress PHP-methods.

Below is the most common way of embedding template parts in a template:

	get_template_part( $slug, $name = null )
    
The two arguments are used to locate a specific filename inside our theme. To replicate what the method `get_header();` does we can use `<?php get_template_part('header'); ?>`. The second argument can be used to look for other versions of the same template part. Let's say we had `header-simple.php` we could use  `<?php get_template_part('header', 'simple'); ?>` to look for that template part first. If not found, Wordpress would instead look for `header.php` as a fallback.