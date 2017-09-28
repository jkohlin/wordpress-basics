## Assignment 1 - Theme setup
Begin by preparing your theme for development and creating the required files.

* **index.php**
  ```
  <?php echo 'Silence is golden.'; ?>
  ```

* **functions.php**
  ```
   <?php 

   //Theme support
   add_theme_support( 'post-thumbnails' );
   add_theme_support( ‘menus’ );

   echo 'Speech is silver. '; 

   ?>
  ```

* **style.css**
```css
    /*
    Theme Name: Portfolio theme
    Author: [Your Name]
    Description: A theme to present creative work
    */
```
* **screenshot.png**
Download and rename from:
http://via.placeholder.com/1200x900/000.png/fff?text=PORTFOLIO%20THEME

### Result
With these four files in place inside your theme folder, you should be able to activate the theme via the admin dashboard. After a successful activation, you should be able to visit your website's homepage and see "Speech is silver. Silence is golden."

**Push your new theme to the remote repository.**
