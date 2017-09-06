## Ecosystem
To better understand how Worpress works under the hood, we will take a look on the database design. 

When installed, Wordpress creates a set of tables with relationships between eachother. One of these tables is **wp_posts** where much of the website's content will be located. Let's take a closer look on this table's fields and structure:

![]({{site.baseurl}}//34.png)

The rows in this table will hold the website's posts, pages and any other content your site is built of. Let's dissect the most important of the fields, and pretend we are looking at an article from a news site.

**ID**
The unique key to this article.

**post_author**
Who wrote this article? A reference ID to the responsible Wordpress user.

**post_date**
When was this article first created?

**post_content**
The article's primary content with text, html and embedded images.

**post_title**
What is the title of this article? e.g. "How Hurricane Irma Became Such a Monster"

**post_status**
Is this article published? Or is it still pending, awating approval? This field can have the following values:

- publish (Live on the website.)
- future (Will be automatically published on a set date and time.)
- draft (Under development and visible only to the author.)
- pending (Awaiting a user with the capability to publish the article.)
- private (Viewable only to WordPress users at Administrator level.)
- trash (Deleted article)

**post_type**
As all content in Wordpress is a post and stored in this table, we need a way of knowing what kind of content each post holds. In this case we are looking at a news article, which could very well be a 'post' post type, which is one of two default types. A developer can define custom post type, and in this case it would be something like 'news' or 'article'.

### Managing posts
Now when we know what a Worpress post look like in the database, we can head over to the admin dashboard where the post is created from.



