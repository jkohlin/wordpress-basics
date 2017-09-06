## Ecosystem
To better understand how Worpress works under the hood, we will take a look on the database design. 

When installed, Wordpress creates a set of tables with relationships between eachother. One table which will be populated during install is **wp_options**. In it, most of the site's settings and configurtion are stored. During install it will be populated with default value rows.

Another table is **wp_posts** where much of the website's content will be located. Let's take a closer look on this table's fields and structure:

![]({{site.baseurl}}//34.png)

The rows in this table will hold the website's posts, pages and any other content your site is built of. All content in Wordpress is a post, and will be found in this table. Let's dissect the most important of the fields, and pretend we are looking at an article from a news site.

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
Is this article published? Or is it still pending awating approval? Can have the following values:

- publish (Live on the website.)
- future (Will be automatically published on a set date and time.)
- draft (Under development and visible only to the author.)
- pending (Awaiting a user with the capability to publish the article.)
- private (Viewable only to WordPress users at Administrator level.)
- trash (Deleted article)

###Posts
**The posts** is central to understand how Wordpress is dealing with content. A post is really just a database entry, with fields like *ID, title and content*. Wordpress uses posts for a lot of things, not only your blog entries.

Let's take a look how the data table for posts are designed:
