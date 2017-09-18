# Users, roles and capabilities

To manage content and settings in Wordpress you need to become a registered user on that specific Wordpress installation. Having a user account in Wordpress is much like a user account on any social platform. You will have a username and basic information about yourself.

You will also have a rank, which controls what information you are allowed to see and edit in admin dashboard. This rank is in Wordpress called **role**.

#### User roles

- Super Admin
- Administrator
- Editor
- Author
- Contributor
- Subscriber

Each of the default roles have different **capabilites** applied to them, which determine what the users with that role are allowed to se and edit. There are hundreds of pre-defined capabilities, which are nothing but names describing the capability.

#### Some of the capabilities
- edit_pages
- edit_posts
- edit_private_pages
- edit_private_posts
- edit_published_pages
- edit_published_posts
- edit_theme_options
- export
- import
- list_users
- manage_categories
- manage_links
- manage_options

### Database
Users are stored in a table called **wp_users**. 

![wp_users table]({{site.baseurl}}/describe-wp_users.png)
*Database table structure*
