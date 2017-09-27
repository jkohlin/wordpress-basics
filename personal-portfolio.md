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

### Project plan
The project is divided into three assignments:

**1. Setup:**
Create the basic theme files required for theme activation.

**2. Content:**
Reading from a content plan and prepare Wordpress using the theme. Adding the content.

**3. Templates:**
Create templates by following wireframe sketches.

## 3 - Content model (post types)

Study the content model plan below and create the required custom post types.

| Title  | Slug | Hierarchial  | Rewrite  |  
|---|---|---|---|
| page *(default)*  | post | true | - |
| post *(default)*  | page | false | - |
| job *(custom)*  | job | false | A single job |

> Registering custom post types: types: https://codex.wordpress.org/Function_Reference/register_post_type
> Wordpress default post types: https://codex.wordpress.org/Post_Types

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


