## The Wordpress post

When Wordpress was new and nothing but a blogging platform, a post in wordpress was equal to a blog entry. Later on posts 

To better understand what posts are, we will take a look on the database design. 

When installed, Wordpress creates a set of tables in the database. One of these tables is **wp_posts** where much of the website's content will be located. Let's dissect what a post really is by looking at the table structure:

![]({{site.baseurl}}//34.png)

The rows in the wp_posts table will hold all the website's content. Let's dissect the most important of the fields, and pretend we are looking at an article from a news site.

**ID**
The unique key to this article.

**post_author**
Who wrote this article? A reference ID to the responsible Wordpress user.

**post_date**
When was this article first published?

**post_content**
The article's primary content with text, html and embedded images.

**post_title**
What is the title of this article?

**post_status**
Is this article published? Or is it still pending, awating approval? This field can have the following values:

- publish (Live on the website.)
- future (Will be automatically published on a set date and time.)
- draft (Under development and visible only to the author.)
- pending (Awaiting a user with the capability to publish the article.)
- private (Viewable only to WordPress users at Administrator level.)
- trash (Deleted article)

**post_type**
As all content in Wordpress is a post and stored in this table, we need a way of knowing what kind of content each post holds. This is because we often want different behavior for each of our content types. Wordpress comes with two default types, 'post' and 'page'.

## Other content fields
A post can hold much more content connected to it, but instead of using fields in the wp_posts table, other tables are used. They will have a many to one relationship with the posts. 

**Post meta**





