##  Assignment 2 - Content
Read through the pre-made content plan below and prepare Wordpress' backend by defining post types, taxonomies and media sizes.

### Post types
The only custom post type you need in the theme is for the creative content. 

**Post type: Project**

| Option | Value |
|---|---|
| hierarchial | false |
| public | true |
| hierarchial | false |
| supports | 'thumbnail', 'title', 'editor,author' |
| taxonomies | 'project_skill', 'project_type' |
| menu_icon | 'dashicons-portfolio' |

### Taxonomies
Your theme must have the following taxonimies registered:

#### Project type

| Option | Value |
|---|---|
| name | 'project_type' |
| object_type | 'project' |
| hierarchial | true |
| label | 'Project types' |

*Example terms: 'Photo', 'Painting', 'Website'*

#### Project skill

| Option | Value |
|---|---|
| name | 'project_skill' |
| object_type | 'project' |
| hierarchial | false |
| label | 'Project skillz' |

*Example terms: 'Sketch', 'Html', 'Javascript'*


> We could use the default post type *post* for the projects, and categorize them using default taxonomies *category* and *tag*. But then if you sometime in the future would want a blog on the website, posts would be filled with projects and the default taxonomies used for other things. So we want to create something new to keep our project content separated.

### Media
A *project* post can hold one image each, which should be stored as the the post's featured image. There are two locations which were the image media will be outputed, in the grid and on single posts/pages.

**Media sizes**

| Name | Size | Crop |
|---|---|--|
| grid_thumbnail | 300x300 | true |
| single_large | 660x400 | false |

### Widget areas (sidebars)
Your theme must have the following widget areas registered:

| Id  |  Name  | Location |
|---|---|--|
| page-sidebar | Page Sidebar | Single pages |

### Theme configuration
Your theme must have support for the following features:

| Feature | Options |
|---|---|
| post-thumbnails | defaults |
| post-formats | defaults |


## Populating content
Now when Wordpress knows about our content's structure, we can start to adding content.

### Pages

| Title  | Content | Thumbnail 
|---|---|---|
| Work | *none* | *none* |
| About | Write something about yourself and add your contact details | A personal photo | 

### Projects

| Title | Content | Thumbnail 
|---|---|---|
| Project title | Describe the project | The project media |
| Project title | Describe the project | The project media |
| ... | ... |

> You can add real project content or a couple of example posts. 

### Site settings

| Setting | Content | 
|---|---|
| Site title | Your first and last name |
| Site description | Describe your website's content |
| Home page | The page 'Work' |

### Custom menus
Build the following custom menus:

| Menu name | Location | Items |
|---|---|---|
| Page menu | `header-nav` | The two pages 'Work' and 'Home' |

### Widgets
Add the following widgets:

| Widget | Sidebar | Content | 
|---|---|---|
| Category widget | Page Sidebar | All terms in `project_skills` taxonomy |

### Assignment handin
1. Prepare Wordpress by adding post types, taxonomies and media sizes. 
2. Register widget areas and theme configurations.
3. Create and publish posts and widgets.

**Push your theme to the remote repository.**

> Tip: If you need help, use Google or Wordpress official Codex: https://codex.wordpress.org/. If stuck please visit the Slack channel and ask for help.
