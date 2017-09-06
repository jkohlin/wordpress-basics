## Ecosystem
To better understand how Worpress works under the hood, we will take a look on the database design. 

When installed, Wordpress creates a set of tables with relationships between eachother. One table which will be populated during install is **wp_options**. In it, most of the site's settings and configurtion are stored. During install it will be populated with default value rows.

Another table is **wp_posts** where much of the website's content will be located. Let's take a closer look on this table's fields and structure:

![]({{site.baseurl}}//34.png)

The rows in this table will hold the website's posts, pages and any other content your site is built of. Let's dissect each of the fields.

**ID**
The primary key of this table, which holds an integer unique to every row.



###Posts
**The posts** is central to understand how Wordpress is dealing with content. A post is really just a database entry, with fields like *ID, title and content*. Wordpress uses posts for a lot of things, not only your blog entries.

Let's take a look how the data table for posts are designed: