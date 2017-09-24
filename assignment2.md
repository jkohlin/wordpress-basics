# Assignment 2 - Personal portfolio

We are going to build a portfolio theme for a personal presentation along with any kind of creative content. The theme will be built as a standalone Wordpress theme, 

### Prerequisites
Before the theme development you will need to have the following:

* A working local wordpress installation
* Git installed locally
* A Github account

## 1 - Project setup
Your theme will be version controlled with Git, and have a personal remote repository on Github. 

1. Generate your personal theme repository via Github Classroom:
https://classroom.github.com/assignment-invitations/ba4e0df3e4a0ef72dbd393bc72ef3b36 
2. Clone the Github repository into your local themes folder (make sure you pick the SSH clone URL).

## 2 - Theme setup
Add the minimum required files in the theme folder, for Wordpress to recognize it as a theme.

#### Tasks
1. Create the following files:
	- your-theme-folder
    		- style.css
       		- functions.php
       		- index.php
        
2. Add the following information to style.css and replace the content with your personal information.
```
	/*
	Theme Name: My Theme Name
	Theme URI: http://farkost.se
	Author: Johan Kohlin
	*/
```

3. Add the following information to index.php as a default template to see the content we create.
```
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
```

4. Save your `style.css` file and activate your new theme via Wordpress Dashboard (Appearence->Theme).

5. Commit and push your new theme back to Github.

## 3 - Content plan
Take a look on the content plan, which describes all pages and post types you will need. 

| Name  | Post type  | Template file  | Content to present  |  
|---|---|---|---|
| Home  |  page | index.php  | Current page |  
| About me  |  page | index.php  | Current page  | 
| My work  | page | portfolio.php | All posts with post type 'job' |
| A sample job  | job | single-job.php | A single job |

1. Register all required post types
2. Create posts, pages and 

## 4 - Templates
Below are the wireframes describing all required templates and their layout. Create them by using Wordpress templates and template parts, and try not to repeat yourself when building them.


