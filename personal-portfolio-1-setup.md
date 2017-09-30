## Assignment 1 - Theme setup
For a Worpdress theme to be recognized and activated via Wordpress there are a couple of files that needs to exists. These are:

* **style.css** - Used for defining the theme name and developer/author (no css rules in here).
* **functions.php** - The file where we keep code to extend Wordpress defaults.
* **index.php** - A default template to render content. (can be empty)
* **screenshot.png** - A screenshot to represent the theme's appearence in Wordpress dashboard.

Begin by preparing your theme for development and creating the required files.

`index.php`:
```
<?php 

echo 'Silence is golden.'; 

?>
```

`functions.php`:
```
 <?php 

 echo 'Speech is silver. '; 

 ?>
```

`style.css`:
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

> Tip: If you need help, use Google or Wordpress Offical Codex: https://codex.wordpress.org/. If stuck please visit the Slack channel and ask for help.
