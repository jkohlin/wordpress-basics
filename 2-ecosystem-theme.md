#Theme
A theme is a set of files with templates and functions controling how the content will be presentated on the frontend. These are the main components of a theme:

- Templates and template parts
- PHP/Wordpress Functions
- Stylesheets and javascripts
- Static asset files
- Theme definition

## Templates and template parts

A Wordpress template is like a blueprint, mixing HTML markup with PHP-methods to retrieve database content.

We can have a multiple set of templates, each with their own layout and functions. So when a Wordpress post is requested by the frontend, Wordpress template system will pick the correct template and render the post content with it, resulting in a HTML-page.

In a theme we need at least one template which should be named `index.php`. This is a fallback template which will be responsible for rendering out content, if no other template is found.

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

Moving on beyond the regular html markup, we aprach next php-block with if-statements and a while-loop.

### Template parts
In the example with `header.php` we were embedding something called a **template part**, which are smaller chunks of reusable template code. Much of our templates will be built by template parts together with HTML and Wordpress PHP-methods.

Below is the most common way of embedding template parts in a template:

	get_template_part( $slug, $name = null )
    
The two arguments are used to locate a specific filename inside our theme. To replicate what the method `get_header()` does, we can use `<?php get_template_part('header'); ?>`. Wordpress will only look in our theme's root directory, so if we had all our template parts in another folder (recommended) we would have to include that folder in the argument too: `<?php get_template_part('my-template-parts/header'); ?>`

The second argument can be used to look for other versions of the same template part. Let's say we had `header-simple.php` where some kind of alternation were made. We could then use  `<?php get_template_part('my-template-parts/header', 'simple'); ?>` to look for that template part first. If not found, Wordpress would instead look for `header.php` as a fallback. The file's naming is important here.
