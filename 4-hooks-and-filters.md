## Hooks and filters

Wordpress comes with a Plugin API which enables developers to extend Wordpress' default behavior. Central in this API is something called *hooks*. Developers can use them to *hook* new code into existing methods, without touching the original code. The Wordpress hook comes in two versions: *action hook* and *filter hook*. They work much like events which we can listen for and do something with when fired.

### Action hooks
Action hooks are defined positions in code, which when reached will fire all actions connected (hooked) to it. When creating an *action*, we tell which action hook to use, and what function to run when that hook is fired. 

#### Adding an action to a action hook
Wordpress core system has many defined hooks which we can use to hook our own functionality to. One of these hooks are called *init* which fires after WordPress has finished loading, but before any headers are sent.

    add_action('init', 'my_cool_function');
    
    	function my_cool_function()  {
      	    //Do something cool when the init hook fires
    	}

#### Defining a new action hook
We can define our own action hooks, and make other developer's life easier when they want to extend or change our code.
	do_action( ‘my_custom_hook’ );

### Filter hooks
Filter hooks are similar but will also pass data from the hook to the hooked functions, which will be returned back to the hook's position. Filter hooks are often defined where data is being echoed, giving us a chance to control that data before being echoed.

#### Adding a filter to a filter hook

    	add_filter( 'author_name', 'reverse_author_name' );
    
    	function reverse_author_name($author_name) {
      	   return strrev($author_name); //Return the filtered content
    	}

#### Defining a filter hook
We can define our own filter hooks, and make other developer's life easier when they want to extend or change our code.

	$this_author = the_author_meta( 'display_name' )
	echo apply_filters('author_name', $this_author); //The filter hook beeing echoed out
    
