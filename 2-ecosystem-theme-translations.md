## Translations

As theme developers we need to prepare our themes for use in different languages. When we are building a theme we are adding new labels, descriptions and namings, in admin dashbord and in templates. To assume these are going to be used in only one specific language is bad practice, so we need to prepare for multiple languges.

This does not mean we have to do any translation, just to make our themes **possible** to be translated into any language.

Wordpress handles translations with something called translation files. These are text based fiels with key/value pairs of strings. The value key holds the value which can be translated, and the key field is what we can use in templates and methods to output the translated string.

In the Wordpress' root we will find a folder called languages, with files for each translated language. For each language we find three files:

`{language}.po`, `{language}.pot`, `{language}.mo`