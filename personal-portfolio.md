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

## 2 - Base files
In the folder you just cloned WE NOW NEED TO ADDthe very basic files required by Wordpress to treat the files as a theme. The files are empty, and it's now up to you to fill them out with the required code.

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

3. Save your style.css file and activate your new theme via Wordpress Dashboard (Appearence->Theme).

4. Commit and push your new theme back to Github.

## 3 - Content types
The main content of our portfolio is the creative material. Personal information and news are going to use the Wordpress default types, posts and pages.

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
