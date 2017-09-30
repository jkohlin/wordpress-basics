## Media

Creating and managing content will often demand some kind of media to back up the text. Wordpress stores media as files, with meta information in the database as posts with the post type *attachment*.

### Featured image
A regular post or page can hold references to attachment in their content field, and thereby mix text with images. Another option is to keep references to media in custom fields (post meta). That enables templates to more easy find representing media for posts without searching through the post content.

A  method for connecting one image to a post is called featured image, and must be manually activated in the theme's `function.php`:

`<?php add_theme_support('post-thumbnails'); ?>`

The post's edit section in the admin dashboard then will have a meta box for selecting an image to connect to that post. This makes it more easy to output images represetning the post.

The attachment id will be stored as post meta.

### Media library
All uploaded images will be listed in the admin dashboard's section *Media*. From there we can manage the images like any other content, and get a good overview of all media available.

### Media sizes
A website will often render same image in different contexts, all with their own space and size limitations. Resizing images on the fly is not very effective, so Wordpress does this for us when we upload an image file.

One uploaded image will be copied into more versions with different sizes and cropping. These variants of our original can be used to output the image in different contexts on the website. The resizing process can only downsize, why keeping the original image large is important. All size variants must be defined beforehand from the theme's `functions.php` or a plugin.

#### Defining an image size
	add_image_size( 'my-custom-imageversion', 1280, 1020, false )

*Arguments are version name, width, height, crop*
    
#### Outputing an image variant:

	wp_get_attachment_image( 321, 'my-custom-imageversion' )

*Arguments are attachment ID, version name*

#### Media storage
When uploading an image into the Wordpress Media Library, a series of events is going to occur:

1. The file is transfered to the web server via ftp protocol.
2. Copies of the image file are created into the defined sizes.
3. A post with post type *attachment* is created with information about the image files.


