# Assignment 2 - Personal portfolio

We are going to build a portfolio theme for a personal presentation along with any kind of creative content. The theme will be built as a standalone Wordpress theme, 

> Note: After the assignment you will have a simple yet fully working Wordpress theme ready to be used on a live website. For further development and maintenance we recommended that you optimize both the theme and development workflow.

### Prerequisites
Before anything else you will need the following:

* A working local wordpress installation
* Git installed locally
* A Github account

## 1 - Project setup
Your theme will be version controlled with Git, and have a personal remote repository on Github. First step is to clone the already existing reposity into the theme-folder of your local Wordpress installation.

#### Tasks
1. Generate your personal theme repository via Github Classroom:
https://classroom.github.com/assignment-invitations/ba4e0df3e4a0ef72dbd393bc72ef3b36 
2. Clone the Github repository into your local themes folder (make sure to pick the SSH clone URL).

## 2 - Theme setup
In the folder you just cloned we now need to add the very basic files required by Wordpress to treat the files as a theme. The files are empty, and it's now up to you to fill them out with the required code.

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

3. Save your `style.css` file and activate your new theme via Wordpress Dashboard (Appearence->Theme).

4. Commit and push your new theme back to Github.


## 3 - Content structure
Study the content plans below and notice the different content types we will need. The types *post* and *page* are default types already added, ergo we only need to add one custom post type - *project*. Our projects could have been added as regular posts, but for this theme we want projects to be distinguished from regular blog posts. You will see why later on.

[Content Plan](http://farkost.se/wordpress-basics/content-plan "Content plan")

#### Tasks
1. In `functions.php`, add a new post type with the following options:
```
$options = array(
      'name' => 'Projects',
      'singular_name' => 'project',
      'public' => true,
      'publicly_queryable' => true,
      'show_ui' => true,
      'query_var' => true,
      'rewrite' => array('slug' => 'projects'),
      'capability_type' => 'post',
      'hierarchical' => false,
      'has_archive' => true,
      'menu_position' => null,
      'supports' => array(
      	'title',
      	'editor',
      	'thumbnail',
      	'comments'
      ),
```

> Read: https://codex.wordpress.org/Post_Types

## 3 - Templates
