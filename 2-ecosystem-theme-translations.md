## Translations

When building themes we are adding labels, descriptions and namings to admin dashbord and to our templates. Hard.coding these in one specific language is bad practice if our theme is not for personal use only. 

As theme developers we need to prepare our themes for use in any language. This does not mean we have to do any translation, just to make our themes **possible** to be translated into any language.

### Translation files
Wordpress handles translations with something called translation files. These are textbased files with key/value pairs of text strings. The value key holds the value which can be translated, and the key field is what we can use in templates and methods to output the translated string.

In the Wordpress' root we will find a folder called languages, with files for each translated language. For each language we find three files:

`{language}.po`, `{language}.pot`, `{language}.mo`

These are different versions of the same content, and contain text strings in that language. When Wordpress is set to a specific languge, the corresponding files are loaded from the language folder and their strings are used.

Just like this we can prepare our themes for translations. By creating a language folder in our theme's folder, with one translation file which will work as a blueprint for translation in outher languages. The keys inside this translation file are what we are using in our themes functions and templates, instead of hard-coded strings.

Example from swedish.po:

Not using localization:

`<?php echo 'your_text'; ?>`

Using localization
	
<?php _e('your_text', 'theme_name'); ?>





