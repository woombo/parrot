Parrot Bootstrap 3
==========

Parrot sits on the shoulders of some great projects. Parrot is a Drupal 7 Mothership subtheme that uses Twitter Bootstrap 3.

What is Bootstrap? http://getbootstrap.com/

How is this theme using Twitter Bootstrap?
The theme uses "some" of the files provided in Bootstrap, to give the theme a structured set of SASS files, as a way to organize the theme's styles. Bootstrap provided the best overall structure that could be generally used for most projects. There are some files removed from the structure, so do not count on this being a 100% working Bootstrap.

## Requirements

* Drupal 7 website
* Mothership base theme http://drupal.org/project/mothership
* LESS installed. The theme uses LESS to build the css.

## Grid System

Bootstrap LESS Grids -- To be updated.

## How do you use the theme?

The theme is not intended to be a *"base theme"*, it is meant to be a *"starter theme"* where you rename it and use it as your theme. The *"base theme"* that is to be used with this theme is the Drupal 7 version of Mothership (http://drupal.org/project/mothership).

To install, copy the folder "parrot" from this repo into /sites/all/themes/ of your Drupal 7 site. Rename the folder to your desired theme name, as well, rename the "parrot.info" file to match the theme name. You will also have to search the "template.php" for "parrot" and replace the name with your new theme name. This name must be lowercase, with no spaces, as it is a machine name. You can then inside the .info file add your Fancy theme title. Renaming is not required for use.

The theme uses SASS to build the CSS, then is compiled into the /css/style.css file. The SASS files are organized in a file structure that is based on overall site structure, not specific components. The structure is as follows in the /css/sass folder:

* /base
* /components
* /layout

Let's look at these folders, and how the SASS files inside each are intended to be used. The files included are based on the Twitter Bootstrap 2.1.1 files, and include *some* of the markup from Twitter Bootstrap. These files include common markup already, as well as SASS Mixins that can be used on your theme.


### The files in /base and their intended use:

* **_code.scss** - This contains the common CSS selectors used to display *Code* visually on your site. If you need to edit or add custom *Code* related CSS, it should be placed in this file.
* **_font-awesome.scss** - This is a `@mixin` file containing icons that can be added to elements. To use this on any CSS selector, use the `@include icon-name;` on the selector, and the icon will be added, as a font based icon. To see the icons included, visit http://fortawesome.github.com/Font-Awesome/. The names are included beside the icon samples.
* **_forms.scss** - This contains the common CSS selectors used to display Forms visually in html. If you need to edit or add custom *Form* related CSS, it should be placed in this file.
* **_mixins.scss** - This is a `@mixin` file containing common and CSS3 styles that can be applied to your theme. To use this on any CSS selector, use the `@include mixin-name;` on the selector, and the *@mixin* will be added. For example `@include inline-block;` will add all the needed css for a IE7+ compatible `display: inline-block;` display. This is where you would add your own custom *@mixin* or find ones to use.
* **_tables.scss** - This contains all common CSS selectors used to display *Tables* visually on you site. If you need to edit or add custom *Table* related CSS, it should be placed in this file.
* **_type.scss** - This contains all *Typography* styles for your site, including base fonts, headings, and more. If you need to edit or add custom *Type* related CSS, it should be placed in this file.
* **_variables.scss** - This contains the *Variables* used in the other CSS selectors, for example, theme specific colors. If you need to edit or add custom *Variables*, they should be placed in this file.


### The files in /base and their intended use:

* **_accordion.scss** - This contains the common CSS selectors used to display *Accordions* visually on your site. If you need to edit or add custom *Accordion* related CSS, it should be placed in this file.
* **_alerts.scss** - This contains the common CSS selectors used to display *Alerts* or *Messages* visually on your site. If you need to edit or add custom *Alert* related CSS, it should be placed in this file.
* **_breadcrumbs.scss** - This contains the common CSS selectors used to display *Breadcrumbs* visually on your site. If you need to edit or add custom *Breadcrumbs* related CSS, it should be placed in this file.
* **_buttons.scss** - This contains the common CSS selectors used to display *Buttons* visually on your site. If you need to edit or add custom *Button* related CSS, it should be placed in this file.
* **_media.scss** - This contains the common CSS selectors used to display all *Media*, like images, videos, flash, audio, overlays, etc type components visually on your site. If you need to edit or add custom *Media* related CSS, it should be placed in this file.
* **_sprites.scss** - This is where you should put the CSS related to *Sprite Images* used on your site.
* **_rotato.scss** - This contains the common CSS selectors used to display *Rototo's* or *Slideshows* visually on your site. If you need to edit or add custom *Rotato* or *Slideshow* related CSS, it should be placed in this file.
* **_labels-badges.scss** - This contains the common CSS selectors used to display *Labels* visually on your site. If you need to edit or add custom *Lable* related CSS, it should be placed in this file.
* **_navs.scss** - This contains the common CSS selectors used to display *Navigation* or *Menus* visually on your site. If you need to edit or add custom *Navigation* related CSS, it should be placed in this file.
* **_pager.scss** - This contains the common CSS selectors used to display *Pager* visually on your site. If you need to edit or add custom *Pager* related CSS, it should be placed in this file.
* **_elements.scss** - This is where you should put the CSS related to the custom *Elements* the do not fall into the files above, which are used on your site.


### The files in /layout and their intended use:

* **_grid.scss** - This contains the *Grid* settings for your site, along with the *Media Queries* for the site. The *Grid* included with the theme by default is the Susy grid framework. You should use this file to layout the sites grid structure as well as block placement. It is recommended to keep the style and placement of block elements separated, allowing quick placement of blocks, and then style is based on the type of block is in the appropriate SASS file.
* **_scaffolding.scss** - This contains the basic *Body* styles that the theme uses. This file is getting the styles from the *Variables* file, and is a great place to declare the base region specific styles, i.e. wrapper backgrounds for the header and footer.


The development of this theme is sponsored in part by ImageX Media.
