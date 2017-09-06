## What is Wordpress?

First and foremost, Wordpress is a tool for *creating and managing content*. As a website owner or editor you will get access to an area hidden from everyone else - the admin dashboard. This is where you write and manage your content. The simple and user friendly interface is what made and still makes Wordpress so popular. From the admin dashboard you get full control over the website, not only editorial content.

### Open source
Who owns Wordpress? The brand and trademark is owned by the Wordpress Foundation, a charitable organisation founded by the author of the code base. The code base is open source, maintained by the community, refering to anyone involved with writing code and taking part in the development. 

Anyone can retrieve the source code for Wordpress and start making improvements. The core developer team will then review your code and might just accept the contribution you made. With hundreds of developers working together, Wordpress is kept relevant and in sync with the ever changing web. 

Every month the Wordpress team will push out new releases, which is important to know when using Wordpress. Your job as a the owner or maintainer of a Wordpress website is to keep up with all updates, and make sure your Wordpress installation using the latest release all the time.

### How it works
What you see when using Wordpress is really just at GUI for the database, with fields and buttons to enter and save data. To store the data a MySQL database is used.

When using Wordpress for public websites, Wordpress will handle the client's HTTP request, fetch content from the database and with that render PHP-based templates. These are returned as HTML-files to the visitors as the HTTP response.

The Wordpress ecosystem is built with PHP which is a server language, meaning you'll need a web server to run Wordpress. Wrapping it up, these are the required components:

 - Web server (commonly used are Ngninx or Apache)
 - PHP (currently version 7.0 or later)
 - MySQL Database
 - HTTPS-support (a security requirement introduced 2017)

Source: https://wordpress.org/about/requirements/

### Hosted vs. Self hosted
The aproach of running Wordpress on your own, by using your own web server or a hosting provider, is in Wordpress terms refered to as 'self-hosted Wordpress'. What that really means is that you are responsible for setting up everything yourself. There are hosting providers which offers easy installs of Wordpress, but in the end of the day it's up to you as the owner for everything to work.

Another aproach to this is using Wordpress.com, a service where Wordpress is already installed and kept updated by a professional team. All you need to do is sign up and you're good to go. You will get a personal URL to your website which makes this solution a quick and easy way to start blogging or running a simple website. The drawback of this solution is that you will have very limited capabilities of the admin dashboard. Therefor you will not be in total control of your website, just your content. This aproach is called 'Hosted Wordpress', and behind the website is a company called Automattic.

### History and future
Wordpress is the open source blogging platform which became the leading content management system (CMS) for websites. It never dropped its blogging capabilities, but from around version 3.0 it came to handle content far beyond just blog posts.

Back in 2001 a guy named Michael Valdrighi created and released a simple weblog tool called b2/Cafelog. It used a new concept of dynamically generating pages from a database, which made it a powerful tool for blogging. After its release Michael suddenly dissapeared and development stalled. Two years later, a developer named Matt Mullenweg took the open sourced sourcecode to b2/Cafelog, and made some changes and improvements to it. Wordpress was born and quickly gained popularity because of its user friendly interface and free of charge.

Today, 14 years later, Wordpress is often considered the standard tool for managing website content. However it has been hugely criticied for beeing unsafe and easy to hack, and is not longer considered to be the lightweight and user friendly alternative.

The CMS world is in the middle of a new shift, towards more lightweight and simple content management, mainly focused on managing content and deliver the data via an API insted of HTML. Beeing an extremely evolving software, Wordpress has already started to introduce a REST API to become the headless CMS.
