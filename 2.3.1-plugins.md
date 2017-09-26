### Wordpress Plugins
We can use a theme's `function.php` to extend Wordpress behavior with hooks without touching the original code. Our own theme methods can be prepared with new hooks to make our theme easy to extend. To extend the current theme from the outside we can use Wordpress Plugins. Plugins runs parallell to the theme and can be managed from the admin dashboard.

We can create our own plugins, or download and install other developers' published plugins. 

## Installing a plugin

1. From the Dashboard we can navigate to Plugins->Add new
2. From here we can search and install any plugin, or upload a previously downloaded plugin.
3. Activate the new plugin.

> When we manually download plugins their file(s) should be placed in the folder `wp-content/plugins` to become visible in the plugin list.

> Wordpress plugins can be browsed from http://wordpress.org/plugins

## Creating a plugin

All we really need is a PHP-file with a plugin header. This header describe the plugin and tell something about the author and licence. But the only required header information is the plugin's name.

    <?php
    /*
    Plugin Name: Reverse author plugin
    */

When placed in the plugin folder, a plugin called *"Reverse authro plugin"* will show up in admin dashboard where a user can turn it on and off.

Now, in same plugin file, we can use the filter hook we made earlier to reverse the author's name on the website.

	<?php
	/*
	Plugin Name: Reverse author plugin
	*/

	add_filter( 'author_name', 'change_site_main_link' );
    
    function reverse_author_name($author_name) {
      return strrev($author_name); //Return the filtered content
    }
    
And our plugin is created! We can do much more, and should probably wrap the code inside a class. But we don't have to.
 
