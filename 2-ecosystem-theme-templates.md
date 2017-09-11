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

The Loop is what we can use to output content in our templates. A global variable called $wp_query will hold the current post's content and also provide helper methods to retrive that content. The content comes in form of an array of posts.

**have_posts()** is a boolean method which will return true as long as there are posts left in the array.

**the_post()** Gets the next post in the array, sets up the post and iterates the loop to next index.By "setting up the post" we can access the content of that post.
