# Assignment 2 - Personal portfolio

We are going to build a new Wordpress theme for a personal portfolio, to present some kind of creative work along with contact and bio. The theme will be built from absolute zero, to contain only the components we really need. The result will be a lightweight theme which you can continue to extend into something more complex later.

### Development prerequisites
* A working local wordpress installation
* Git installed locally
* A Github account

## 1 - Project setup
Your theme will be version controlled with Git, and have a personal remote repository on Github controlled by your teacher. To present your current work, all you need to do is push to remote repository.

1. Generate your personal theme repository via Github Classroom:
https://classroom.github.com/assignment-invitations/ba4e0df3e4a0ef72dbd393bc72ef3b36 
2. Clone the Github repository into your local themes folder (make sure you pick the SSH clone URL).
3. Replace the content in style.css with your personal information. Save the file.
4. Activate your new theme via Wordpress Dashboard (Appearence->Theme).
5. Commit and push your new theme back to Github.

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


