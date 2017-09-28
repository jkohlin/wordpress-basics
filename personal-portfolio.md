# Project - Personal portfolio theme
You are going to build a new Wordpress theme for a personal portfolio, to present some kind of creative work along with contact and bio. The theme will be built from scratch, and you will add only the absolute required components. The result will be a very lightweight and simple theme which you can use as it is, or extend into something more complex.

In the assignment only the theme folder will be version controlled with Git.

### Prerequisites
* A working local Wordpress installation
* Git installed locally
* A Github account
* Personal repository via Github Classroom

### Github Classroom
Github Classroom will be used as your remote Git repository, where your teacher can follow and comment on your work. You will work in your local environment and push to the remote repository after each assignment.

1. Generate your personal theme repository:
https://classroom.github.com/assignment-invitations/ba4e0df3e4a0ef72dbd393bc72ef3b36 
2. Clone the Github repository into your local themes folder (make sure you pick the SSH clone URL).

## Assignment 1 - Theme setup
Begin by preparing your theme for development and creating the required files.

* **index.php**
  ```
  <?php echo 'Silence is golden.'; ?>
  ```

* **functions.php**
  ```
   <?php 

   //Theme support
   add_theme_support( 'post-thumbnails' );
   add_theme_support( ‘menus’ );

   echo 'Speech is silver. '; 

   ?>
  ```

* **style.css**
```css
    /*
    Theme Name: Portfolio theme
    Author: [Your Name]
    Description: A theme to present creative work
    */
```
* **screenshot.png**
Download and rename from:
http://via.placeholder.com/1200x900/000.png/fff?text=PORTFOLIO%20THEME

### Result
With these four files in place inside your theme folder, you should be able to activate the theme via the admin dashboard. After a successful activation, you should be able to visit your website's homepage and see "Speech is silver. Silence is golden."

**Push your new theme to the remote repository.**

---

##  Assignment 2 - Content
The content is central and should control the presentation of both the backend and frontend views. A Wordpress theme can adapt both frontend templates and admin dashboard. Below is the content plan, where we find which post types and taxonomies we need to prepare for.

[Link to content plan]

#### Tasks
1. Register all required post types and taxonomies from the content plan.
1. Define the required image sizes.
2. Create and publish all posts via admin dashboard.

**Push your new theme to the remote repository.**

## Assignment 3 - Templates
#### Wireframes
The wireframes sketches explains the website's different views, and how content is layed out on them. From that we can see the common elements we need to create as template parts.

[Link to wireframes pdf]

Some elements will follow all these 

**Job post type**

| Option | Value |
|---|---|
| name | Jobs |
| slug | job |
| rewrite | true |
| hierarchical | false |
| taxonomies | job_type |

## 4 - Adding Content
Take a look on the content plan below, and begin by register all custom post types.

### Hierarchial posts (pages)
| Title  | Post type  | Template  |
|---|---|---|
| Home  |  page | Default  | 
| About me  |  page | Default  |
| My work  | page | Portfolio |

### Non-hierarchial posts
| Title  | Post type  |
|---|---|
| My first job  | job |
| My second job  | job |
| My first blog post  | post |
| My second blog post  | post |

### Templates
| Name | Template file  | Content to present  |  
|---|---|---|
|   | single-job.php | A single job |
| My second job  | single-job.php | A single job |
| My first blog post  | single.php | A single blog post |
| My second blog post  | post | single.php | A single blog post |

## 4 - Templates
Below are the wireframes describing all required templates and their layout. Create them by using Wordpress templates and template parts, and try not to repeat yourself when building them.


