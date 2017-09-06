## Ecosystem
To better understand how Worpress works under the hood, we will begin take a look on the database design. When installed, Wordpress creates a set of tables with relationships between eachother.

One of the most important table is **wp_posts** where much of your website's content will be located. Let's take a closer look on this table:

![]({{site.baseurl}}//34.png)

###Posts
**The posts** is central to understand how Wordpress is dealing with content. A post is really just a database entry, with fields like *ID, title and content*. Wordpress uses posts for a lot of things, not only your blog entries.

Let's take a look how the data table for posts are designed:

