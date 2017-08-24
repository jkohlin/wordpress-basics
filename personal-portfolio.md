# Assignment 2 - Personal portfolio

We are going to build a portfolio theme for a personal presentation along with any kind of creative content. The theme will be built as a standalone Wordpress theme, 

> Note: After the assignment you will have a simple yet fully working Wordpress theme ready to be used on a live website. For further development and maintenance we recommended that you optimize both the theme and development workflow.

### Prerequisites
Before anything else you will need the following:

* A working local wordpress installation
* Git installed locally
* A Github account

## 1 - Project setup
---
Your theme will be version controlled with Git, and have a personal remote repository on Github. First step is to clone the already existing reposity into the theme-folder of your local Wordpress installation.

#### Tasks
1. Generate your personal theme repository via Github Classroom:
https://classroom.github.com/assignment-invitations/ba4e0df3e4a0ef72dbd393bc72ef3b36 
2. Clone the Github repository into your local themes folder (make sure to pick the SSH clone URL).

## 2 - Base files
In the folder you just cloned into your themes folder you'll find the very basic files required by Wordpress to treat the files as a theme. The files are empty, and it's now up to you to fill them out with the required code.

#### Tasks
1. Create the following files:
	- your-theme-folder
    	- style.css
        - functions.php
        - index.php
        
2. Add the following information to style.css and replace the bolded text with your personal information.

```/*
Theme Name: My Theme Name
Theme URI: http://wordpress.org/themes/twentythirteen
Author: the WordPress team
Author URI: http://wordpress.org/
Description: The 2013 theme for WordPress takes us back to the blog, featuring a full range of post formats, each displayed beautifully in their own unique way. Design details abound, starting with a vibrant color scheme and matching header images, beautiful typography and icons, and a flexible layout that looks great on any device, big or small.
Version: 1.0
License: GNU General Public License v2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Tags: black, brown, orange, tan, white, yellow, light, one-column, two-columns, right-sidebar, flexible-width, custom-header, custom-menu, editor-style, featured-images, microformats, post-formats, rtl-language-support, sticky-post, translation-ready
Text Domain: twentythirteen

This theme, like WordPress, is licensed under the GPL.
Use it to make something cool, have fun, and share what you've learned with others.
*/```

## 3 - Post types
We need to make sure Wordpress knows about what kind of content we will be using. For this project we only need one custom post type - *projects*. It will be used for storing our creative content.

#### Custom Post types
| Name  | Slug | Template | Purpose |
|---|---|---|---|
| Project  | project | Project (single-project.php) | To show of your work. |

#### Tasks
1. In functions.php, register the new post type and make sure it shows up in your Wordpress Dashboard menu.

## 3 - Content and structure
---

It's time to create the backbone of our website - the content. Follow the structure plan below and create the pages. Enter som placeholder content and publish the pages.

#### Pages
| Title  | Template  | Purpose  |
|---|---|---|
| Home  | Default | List all projects.  |
| About  | Default | Personal description and following options.  |
| Contact  | Default | Contact information and form.  |

> Note: For now all pages will use the default template (index.php).

#### Tasks
1. Create the pages from the content plan above, and add some short but descriptive example text in their content field.
2. Add two example posts within the projects post type, and add some short but descriptive example text in their content field.

## 3 - Template
---

Now when we have some content to work with, let's create the templates to display it. At the moment all of our three pages uses the default template that came with out starter theme. That is enough to
