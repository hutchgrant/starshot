# Drupal 8 Bootstrap Small Business theme

This is a Bootstrap Drupal 8 theme for a small business. The example provided is for a printing/merchandise retailer.

## Demo

Here's a [live example](https://www.starcustomproducts.ca)

## Manual Install

- extract starshot to siteroot/themes/
- copy "starshot_mod" folder from theme and place in your drupal siteroot/modules directory
- download [bootstrap 3 source](https://github.com/twbs/bootstrap/archive/v3.3.7.zip) extract to siteroot/themes/starshot/ rename folder to "bootstrap"
- download, extract and enable: bootstrap, captcha, recaptcha, libraries, slick, slick_ui, blazy
- enable starshot_mod

## Drush install

Make sure you've copied the "starshot_mod" folder into your siteroot/modules directory before running drush.

```
drush pm-enable bootstrap, captcha, recaptcha, libraries, slick, slick_ui, blazy -y
drush pm-enable starshot_mod
drush config-set system.theme default bootstrap -y
drush pm-uninstall bartik -y
drush pm-enable starshot -y
drush config-set system.theme default starshot -y
```

## blazy library

- download [blazy](https://github.com/dinbror/blazy/) and place in your siteroot/libraries folder. If libraries directory doesn't exist, create it.
- make sure to rename the blazy folder from blazy-master to "blazy" and the path siteroot/libraries/blazy/blazy.min.js is correct

## Block Configure

In structure->block layout you will want to place the following blocks:

Navigation:
- Site branding

Navigation(Collapsible)
- Main Navigation
- User account menu

Top Bar:
- Breadcrumbs
- Primary admin actions
- Status messages
- Tabs
- Page title

Content:
- Main Page content

Footer:
- footer (menu) *Place at top of stack and make the machine name starshot_footer

You may also(ideally) wish to make the blocks "address_map", "featurettes", "copyright", into custom blocks so that you can dynamically alter them at any time.  Simply copy the contents of each block.block.starshot_anyblockname from starshot/templates/block (without the twig templates e.g. everything between {% block content %} and {% end content %} ), paste it into a new custom block then place the new block into the block layout.


## Services Configure

Adjust Slick options
configuration -> slick

- add optionset

structure -> content types -> service(1, 2) > manage display(tab)
- adjust image field(slick) display settings of service content type

## License

starshot theme is available under the [Apache 2.0 License](https://github.com/hutchgrant/starshot/blob/master/LICENSE).

## Contributing

All contributions will be placed under the same Apache 2.0 license, contributers must agree to that license.
For more information see [contributing](https://github.com/hutchgrant/starshot/blob/master/CONTRIBUTING.md).

## Author

**Grant Hutchinson (hutchgrant)**
