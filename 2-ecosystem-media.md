## Media

Creating and managing content will often demand some kind of media to back up the text. Wordpress comes with a manager for upload and manage files, focusing on image content.

Distributing content to different channels, networks and devices requires an adaptive aproach to fit each situation. The image size and resolution is one factor which we need a plan for, often including having many version of same image.

When uploading an image into the Wordpress Media Library, a chain of events is going to occur:

1. The file is transfered to the web server.
2. Copies of the image file are created with different cropping, size and resolution.
3. A post with post type *attachment* is created with information about the image files.

The details about the copying and resizing part is made from blueprints created by the theme developer, and will apply to all future image uploads.