## Widgets

Widgets are small content/functionality blocks that can be added and controlled from the admin dashboard. They are placed into **widget areas** by a drag-and-drop interface. A theme can have one or many widget areas, which have to be defined by the theme developer.

![Wordpress widgets]({{site.baseurl}}//wordpress-widgets1.png)

The main benefit of widgets is that they let us add content and functionality not bound to . specific page or post, but rather theme positons. We as theme developers define these positions as widget areas, and choose where in our templates they are shown. The posts and pages using templates with widget ares, will then show all the widgets applied to these.

A common widget is the *Search field*, which in the admin area let's the editor or admin choose the title and the button text of the search form. This widget is often applied to widget areas in header.php, which will be included by all templates.

### Developer workflow
1. Register widget areas (sidebars) in `functions.php:
		
```
<?php
/**
 * Register our sidebars and widgetized areas.
 *
 */
function my_widgets_init() {

	register_sidebar( array(
		'name'          => 'Header Right Sidebar',
		'id'            => 'header-right-sidebar'
	) );

}
add_action( 'widgets_init', 'my_widgets_init' );
?>
```

2. Output the widget area (sidebar) in template:

```
<ul id="sidebar">
		<?php dynamic_sidebar( 'header-right-sidebar' ); ?>
</ul>
```
