##  Assignment 2 - Content plan
Planning our content is important as we need to prepare Wordpress to handle it. Read through the content plan below and prepare Wordpress by describing post types, taxonomies and media.

### Post types
The only custom post type you need in the theme is for the creative content. We could use the default post type *post* for them, and categorize them using default taxonomies *category* and *tag*. But then if you sometime in the future would want a blog on the website, posts would be filled with projects and the default taxonomies used for other things. So we want to create something new to keep our project content separated.

**Post type: Project**
Your creative content will be stored as posts with the custom post type *project*.

| Option | Value |
|---|---|
| hierarchial | false |
| public | true |
| hierarchial | false |
| supports | 'thumbnail', 'title', 'editor,author' |
| taxonomies | 'project_skill', 'project_type' |
| menu_icon | 'dashicons-portfolio' |

---

**Taxonomies**
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

---

#### Media
A *project* post can hold one image each, which should be stored as the the featured image. There are two locations which were the image media will be outputed, in the grid and on single posts/pages.

**Media sizes**

| Name | Size | Crop |
|---|---|--|
| grid_thumbnail | 300x300 | true |
| single_large | 660x400 | false |

---

#### Theme configuration
`add_theme_support( 'post-thumbnails', array( 'project', 'page' ) );`

### Adding content
Create the two pages and use the default page template (index.php) for now.

| Page title | Template |
|---|---|
| Work | Default |
| About | Default |

For the projects you can add material from your previous portfolio, or add some example projetcs just to see something in the templates. You can remove these later.

### Tasks
1. Prepare Wordpress by adding post types, taxonomies and configurations.
2. Create and publish all posts via admin dashboard.

**Push your theme to the remote repository.**

> Tip: If you need help, use Google or Wordpress Offical Codex: https://codex.wordpress.org/. If stuck please visit the Slack channel and ask for help.
