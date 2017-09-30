##  Assignment 2 - Content plan
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
The projects are categorized by type. The terms can be something like "Photo", "Illustration", "Website". A project will most of the times have only one term.

Other information about the project, like applications used or specific technologies or methods will use another taxonomy.

#### Taxonomy: Project type

| Option | Value |
|---|---|
| name | 'project_type' |
| object_type | 'project' |
| hierarchial | true |
| label | 'Project types' |

#### Taxonomy: Project skill

| Option | Value |
|---|---|
| name | 'project_skill' |
| object_type | 'project' |
| hierarchial | false |
| label | 'Project skillz' |

> We could use the default post type *post* for the projects, and categorize them using default taxonomies *category* and *tag*. But then if you sometime in the future would want a blog on the website, posts would be filled with projects and the default taxonomies used for other things. So we want to create something new to keep our project content separated.

### Media
A *project* post can hold one image each, which should be stored as the the post's featured image. There are two locations which were the image media will be outputed, in the grid and on single posts/pages.

**Media sizes**

| Name | Size | Crop |
|---|---|--|
| grid_thumbnail | 300x300 | true |
| single_large | 660x400 | false |


### Theme configuration
Some features are disabled by default, so you need to activate them via the theme's `functions.php`.

`add_theme_support( 'post-thumbnails');`

`add_theme_support( 'post-formats');`


### Pages
| Page title | Template | 
|---|---|
| Work (homepage) | Default |
| About | Default |

> You can edit the templates later when you have them.

### Projects
For the project content you can add real material, or publsih some example projetc posts just to see something in the templates. 

### Tasks
1. Prepare Wordpress by adding post types, taxonomies and configurations.
2. Create and publish all posts via admin dashboard.

**Push your theme to the remote repository.**

> Tip: If you need help, use Google or Wordpress official Codex: https://codex.wordpress.org/. If stuck please visit the Slack channel and ask for help.