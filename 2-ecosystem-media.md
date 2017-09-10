## Media

Creating and managing content will often demand some kind of media to back up the text. Wordpress comes with a manager for upload and manage files, focusing on image content.

Distributing content to different channels, networks and devices requires an adaptive aproach to fit each situation. The image size and resolution is one factor which we need a plan for, often including having many version of same image.

The developer of a theme will on forehand have to define which sizes will be needed, and carefully plan for different resolutions and devices. Each size get an unique name, which are used 

When uploading an image into the Wordpress Media Library, a series of events is going to occur:

1. The file is transfered to the web server via ftp protocol.
2. Copies of the image file are created into the defined sizes.
3. A post with post type *attachment* is created with information about the image files.

Using 
