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
3. Replace the content in style.css with your personal information. Save the file.
4. Activate your new theme via Wordpress Dashboard (Appearence->Theme).
5. Commit and push your new theme back to Github.

## 3 - Content model (post types)
| Title  | Slug | Hierarchial  | Supports  |  
|---|---|---|---|
| page *(default)*  | job | true | A single job |
| post *(default)*  | job | false | A single job |
| job *(custom)*  | job | false | A single job |

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


