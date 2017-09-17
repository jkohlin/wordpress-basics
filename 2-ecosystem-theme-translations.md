## Translations

When building themes we are adding labels, descriptions and namings to admin dashbord and to our templates. Hard.coding these in one specific language is bad practice if our theme is not for personal use only. 

As theme developers we need to prepare our themes for use in any language. This does not mean we have to do any translation, just to make our themes **possible** to be translated into any language.

### Translation files
Wordpress handles translations with something called translation files. These are textfiles with key/value pairs of strings. The value-field holds the string which can be translated, and the key field is what we use in theme to output the translated string.

In the Wordpress' root a folder called languages holds language files for Wordpress' defaults. The same principle applies to a theme, where we can have theme-specific translation files. Each language is represented by three files:

`{language}.po`, `{language}.pot`, `{language}.mo`

These files are just different versions of the same content, and will load when that specific language is defined in the current Wordpress configuration.

Example from swedish.po:

    #sidebar.php:8
      msgid "About the author"
      msgstr "Om författaren"

In sidebar.php, we can output the current translation with:
	
	<?php _e('About the author', 'my_theme_name_domain'); ?>

The second argument is a string which adresses the current translation context. In a theme we can define a context and which folder to use in the very top of `functions.php`:

	<?php load_theme_textdomain('my_theme_name_domain', get_template_directory() . '/languages'); ?>





