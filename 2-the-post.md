## The Wordpress Post
The Wordpress Post is a general data model which is used to hold Wordpress content. Almost any content in Wordpress is some kind of post, and stored in the same database table. However, in the Wordpress Dashboard different post types are separated into their own sections, to simplify content management.

As default we are dealing with the following fields for a Wordpress post:

**ID**
The unique key to this post.

**post_author**
Who created this post? A reference ID to the responsible Wordpress user.

**post_date**
When was this post first published?

**post_title**
What is the title of this article?

**post_content**
The post's primary content with text, links and media references

**post_status**
Is this article published? Or is it still pending, awating approval? This field can have the following values:

- publish (Live on the website.)
- future (Will be automatically published on a set date and time.)
- draft (Under development and visible only to the author.)
- pending (Awaiting a user with the capability to publish the article.)
- private (Viewable only to WordPress users at Administrator level.)
- trash (Deleted article)

**post_type**
As all content in Wordpress is a post and stored in this table, we need a way of knowing what kind of content each post holds. 

### Post Format
When rendering content we sometimes need to adapt the layout to fit the specific content. *Post format* is a value which set by the author when creating the content. There are a number of pre-set values available and we are limited to use one of the values to describe our content. The currently available values are:

aside
gallery
link
image
quote
status
video
audio
chat
Source: https://codex.wordpress.org/Post_Formats

> The post format value itself does not control any behavior or layout. It's all up to you as a theme developer what to do with the information.

### The database
All posts are stored in the MySQL database in a table called **wp_posts**.
