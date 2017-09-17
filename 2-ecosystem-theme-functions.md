## Functions

Every theme are required to have a file called functions.php. This file is where we as theme developers to control Wordpress default behavior. In this file we can register new post types, define widget areas, control asset loading, create and extend PHP-methods and much more. Everything we do in this file will only apply when the theme containing it is activated.

In a way it makes our theme into a plugin, which will control the current Wordpress installation's behavior. All the functionality in functions.php will excecute on each frontend request, and will load right after our active plugins.

A good practice is to not have functionality written directly into functions.php, but instead create a new folder with separated PHP-files, then in functions.php include these with PHP.

