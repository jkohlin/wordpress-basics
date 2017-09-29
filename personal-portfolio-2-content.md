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

#### Media sizes
A *project* post can hold one image each, which should be stored as the the featured image. There are two locations which were the image media will be outputed, in the grid and on single posts/pages.

| Name | Size | Crop |
|---|---|--|
| grid_thumbnail | 300x300 | true |
| single_large | 660x400 | false |

#### Theme configuration
`add_theme_support( 'post-thumbnails', array( 'project', 'page' ) );`

#### Pages
| Page title | Template | Content |
|---|---|---|
| Work | portfolio.php | List projects |
| About | page.php | Featured image and page content |

#### Projects
| Project title | Template | Content |
|---|---|---|
| My first project | single-project.php | Dummy text content and featured image |
*Add about 10 project posts with different content and images*

### Tasks
1. Register all required post types and taxonomies from the content plan.
1. Define the required image sizes.
2. Create and publish all posts via admin dashboard.

**Push your theme to the remote repository.**

> Tip: If you need help, use Google or Wordpress Offical Codex: https://codex.wordpress.org/. If stuck please visit the Slack channel and ask for help.
