## Media

Creating and managing content will often demand some kind of media to back up the text. Wordpress comes with a manager for upload and manage files, focusing on image content.

Distributing content to different channels, networks and devices requires an adaptive aproach to fit each situation. The image size and resolution is one factor which we need a plan for, often including having many version of same image.

The developer of a theme will on forehand have to define these image sizes, and carefully plan for different resolutions and devices. Each size gets a unique name, which are used in the templates to output the correct image version.

Defining image size (`functions.php`):

	add_image_size( 'my-custom-imageversion', 1280, 1020, false )

*Arguments are name, width, height, crop*
    
Outputing an image (`any-template.php`):

	wp_get_attachment_image( 321, 'my-custom-imageversion' )

*Arguments are ??, size-definition-name*
[comment]: <> (Vad är 321 i anropet ovan?)
When uploading an image into the Wordpress Media Library, a series of events is going to occur:

1. The file is transfered to the web server via ftp protocol.
2. Copies of the image file are created into the defined sizes.
3. A post with post type *attachment* is created with information about the image files.

Each image will be represented in the Media Library as one single image. This way a content editor won't have to worry about sizes and multiple variants.


