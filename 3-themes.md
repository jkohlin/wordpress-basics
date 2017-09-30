## Themes

We use Wordpress themes to extend Wordpress default behavior, and define how the content will be presented on the frontend. A Wordpress installation can have many themes, but only one can be active. An admin can easily switch between themes and thereby the website's appearence.

### Theme components
Each theme holds templates, stylesheets and functions. They are encapsulated into a theme folder which is placed in the Wordpress installation within a folder called `wp-content/themes/`. 

**Templates**: File describing how to render content on the frontend website.
**Functions**: PHP-code to extend Wordpress default behavior.
**Assets**: Stylesheets, fonts, scripts and images to control the visual appearance on the frontend.

### Downloading themes
There is a countless number of themes available for free of charge, which we can download and customized using well prepared dashboard settings. This makes it easy for anyone to create a Wordpress website and get the desired appearence and feel.

### Building themes
When building new themes, we have to pick a development strategy. Should we build it from scratch, or base it on another theme?

#### Child theme
Wordpress enables us to make changes to a theme, without touching the theme's files. It's done by creating something called child theme, which inherits all theme code from another (parent) theme. The child theme can then include ony the parts we want to override and extend. If the parent theme is released in new versions, an update would then not affect the custom code in the child theme.

#### Starter themes
Starter themes are standalone themes witch basic templates and functionality ment to be continued on by a developer. When building many themes, this can be a good starting point to avoid repetitive tasks.

We can create our own starter themes, suiting our exact needs. Or we can pick some of the open source starter themes available, which are well tested, updated and a robust starting point for any new theme project. One of the most popular starter themes is [Underscores](http://underscores.me/ "Underscores project").

#### Building from scratch
By building a new theme from scratch we get only the parts we really need for the website and a better understanding of the theme. This is the method we will be using in this course.
