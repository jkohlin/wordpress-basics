# Assignment 2 - Personal portfolio

We are going to build a portfolio theme for a personal presentation along with any kind of creative content. The theme will be built as a standalone Wordpress theme, meaning we will not extend or adjust an already built theme, instead we will build it from scratch.

> Note: After the assignment you will have a simple yet fully working Wordpress theme ready to be used on a live website. For further development and maintenance we recommended that you optimize both the theme and development workflow.

### Prerequisites
Before anything else you will need the following:

* A working local wordpress installation
* Git installed locally
* A Github account

## 1 - Theme setup
---

#### Tasks
1. Generate your personal theme repository:
https://classroom.github.com/assignment-invitations/ba4e0df3e4a0ef72dbd393bc72ef3b36 
2. Clone the Github repository into your local themes folder (make sure to pick the SSH clone URL).
3. Change the theme's name to anything you want, and perform a `git push` to the Github repository.
4. Activate your new theme from Wordpress admin.

## 2 - Post types
We need to make sure Wordpress knows about what kind of content we will be using. For this project we will need only one custom post types, 'projects'. 

#### Custom Post types
| Name  | Slug | Template | Purpose |
|---|---|---|---|
| Project  | project | Project (single-project.php) | To show of your work. |

#### Tasks
1. In functions.php, register the new post type and make sure it shows up in your Wordpress Dashboard menu.



## 3 - Content and structure
---

It's time to create the backbone of every website, the content. Follow the structure plan below and create the content via Wordpress dashboard.

#### Pages
| Title  | Template  | Purpose  |
|---|---|---|
| Home  | Default (index.php) | List all projects.  |
| About  | Page (page.php)  | Personal description and following options.  |
| Contact  | Page (page.php)  | Contact information and form.  |

> Note: For now all pages will use the default template (index.php).


#### Tasks
1. Create the pages from the content plan above, and add some short but descriptive example text in their content field.
2. Add two example posts within the projects post type, and add some short but descriptive example text in their content field.

## 3 - Styleguide
---

As shown in the content plan, we will need two
