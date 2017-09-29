##  Assignment 2 - Content plan
Below is the content plan, where you can find which post types and taxonomies you need, and what content to create. You can add more/different content later, but stick to the plan for now.

### Post types
The only content we need to prepare for is the projects. We could use the default post type *post* for them, and categorize them using default taxonomies *category* and *tag*. But then if we sometimes in the future would decide to add a blog on the same website, posts would be filled with projects. And we want to keep different content separated.

You need to create a custom post type called *project*, and two new taxonomies to keep them ordered.

**Post type: Project**

| Option | Value |
|---|---|
| hierarchial | false |
| public | true |
| hierarchial | false |
| supports | 'thumbnail', 'title', 'editor,author' |
| taxonomies | 'project_skill', 'project_type' |
| menu_icon | 'dashicons-portfolio' |

---

**Custom taxonomies**

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
