Mautic Drupal 6.x module
========================

This Drupal 6 module lets you add the Mautic tracking gif image to your Drupal website and embed Mautic forms in Drupal content.

### Installation

1. [Download](https://github.com/mautic/mautic-drupal/archive/6.x.zip) zip package.
2. Unzip downloaded file to your drupal instance into `sites/all/modules`. ([read more](https://www.drupal.org/documentation/install/modules-themes/modules-5-6))
3. Go to **Administer** / **Site building** / **Modules**
4. **Mautic Integration** module should be at the bottom. Enable it.
5. Go to **Administer** / **Mautic** and insert Mautic Base URL. Save it.
6. Go to **Administer** / **Site building** / **Blocks** and drag & drop Mautic Tracker from **Disabled** into **Footer** position. Save blocks.

### Mautic Tracking Image

Module will insert 1 px gif image loaded from your Mautic instance. You can check HTML source code (CTRL + U) of your Joomla website to make sure the plugin works. You should be able to find something like this:

`<img src="http://yourmautic.com/mtracking.gif" />`

There will be probably longer URL query string at the end of the tracking image URL. It is encoded additional data about the page (title, url, referrer, language).

### Form embed

To embed a Mautic form into Drupal content, insert this code snippet:

`{mauticform id=ID width=300px height=300px}`

ID is the identifier of the Mautic form you want to embed. You can see the ID of the form in the URL of the form detail. For example for www.yourmautic.com/forms/view/1, ID = 1.
