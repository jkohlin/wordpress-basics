## Theme types

A popular aproach when building themes is to make changes in an already existing theme, to get the prefered appearance and functionality. If the theme's licence aproves, we can do this by simply editing directly in the theme files. We can of course also extend the theme by adding more code or templetes to it.

Most published themes will sooner or later have updates available, which are simple to make via the admin dashboard. However, if any changes were made directly in the theme files, these would become overwritten when performing the update, leaving us with the misery of undone work.

### Child theme
Wordpress has solved this by introducing *child themes*, which enables us to make all changes as a separate theme, without touching the main theme (parent theme). Updates can vice-versa be made on the main theme, without touching our changes in the child theme. While this aproach is preferable and more safe, a complete understanding of the main theme is prefered to extend it effectively. A child theme is also depending on the main theme, and can never exist on it's own.

### Starter themes
When we have a lot of custom styles and functionality, we might be better of building ourself a brand new theme. This involves creating all files and folders, adding each line of code ourself. Fair enough - if we were doing this only once. But when we create a lot of themes, we find ourself doing much of the work over and over again. To avoid these repetitive tasks, we need some kind of starter kit. These are called *starter themes* and includes the most basic templates, functions and styles for us to build further on.

We can create our own starter theme, suiting our exact needs. Or we can pick some of the open source starter themes available, which are well tested, updated and a robust starting point for any new theme project. One of the most popular starter themes is [Underscores](http://underscores.me/ "Underscores project"). Go check it out!

### Building from scratch
The previous development types will always contain a little more code than you really need for a specific theme. They are methods for development speed. By building a theme from scratch we get only the parts we really need for the website and a better understanding of the theme. This is the method we will be using when building our new portfolio theme.
