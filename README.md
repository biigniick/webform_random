Description
-----------
This module provides a checkbox on the WebformForm Form Settings page located
located at /node/%/webform/configure to display the form elements randomly.

Requirements
------------
[Drupal 7.x](https://www.drupal.org/project/drupal)
[Webform](https://www.drupal.org/project/webform)

Installation
------------
1. Copy the entire webform_random directory the Drupal sites/all/modules directory.
2. Login as an administrator. Enable the module in the "Administer" -> "Modules"
3. Enable the "Randomize form elements" setting on the "WebForm" -> "Form Settings" tab

Known Issues!
------------
### [Saving configuration on form settings page doesn't work as expected](https://www.drupal.org/node/2906016)
On the form settings page (node/%/webform/configure), clicking 'Save configuration' will only save the checkbox for webform random and none of the other changes get saved.

Workaround:
1. disable Webform Random
2. make changes to your settings as desired
3. enable Webform Random

it has something to do with line 21 of webform_random.module
```php
    //  SOMETHING NOT WORKING CORRECTLY HERE
    $form['actions']['submit']['#submit'][] = 'webform_random_save_submit';
```
---
Support
-------
File bugs with this module on Drupal.org at [Issues for Webform Random](http://drupal.org/project/issues/webform_random)

