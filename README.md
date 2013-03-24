# vanilla

Personal starting point for new web projects.

## Structure

General directory structure:

    README.md
    _assets/
      css/
      html/
    _vanilla-template.kit
    styleguide/

## HTML

### _vanilla-template.kit

Template file for new page `.kit` files.

HTML 5 elements found in the document are optimally structured for a “one-web” approach. They contain ARIA Landmark Roles which provide accessibility to those that rely on assistive technology. `role=complimentary` is the only one that will likely be moved, removed, or attached to a different element.

Any extra `<head>` content should be imported below the `html-head.kit` import.

### _assets/html

The `html` directory contains reusable HTML snippets used globally. These files should also be unique to each project. All page specific HTML should be grouped together in respectively titled directories in the root folder.

Directory example:

    html/
      partials/
        _ga-id.kit
      landing page/
        kits/

### Kit directories

All `.kit` directores should contain HTML convertable `*.kit` files for the respective pages. For example:

    styleguide/
      basic-styles.html
      form-styles.html
      kits/
        basic-styles.kit
        form-styles.kit
        styleguide.kit
        ui-styles.kit
      styleguide.html
      ui-styles.html

## CSS

### _assets/css

The `page` directory contains page named directories and their respective stylesheets to be imported. A `sass` directory to contain all page `.scss` files.

Directory example:

    css/
      _vanilla.scss
      page/
        landing page/
          sass/
            landing-page.scss
          landing-page.css

#### SASS Variables

`_vars.scss` over-writes framework variables and sets project variables. There should never be a need to modify any framework code. This file also imports `_morula.scss` from [morula](https://github.com/inriverie/morula) which is a cross project variable library.

#### Page specific stylesheets

At the top of each `[page].scss` file shoud be the name of the CSS file followed by a section to re-define framework variables:

    /*------------------------------------*\
        NAME OF PAGE
    \*------------------------------------*/
    /**
     * Re-define framework and Vanilla variables
     */

The only required import should be the `_vanilla.scss` file. This contains all the base default variables, styles, etc… If the page uses any framework objects, import them after `_vanilla.scss`.

    /**
     * Import all of the things...
     */
    @import "../../../vanilla.scss";

Lastly, there's a section dedicated to styles specific to the page the CSS file will be linked to.

    /**
     * Custom page styles
     */

## Global imports

All pages should include the following:

* `_global-vars.kit`
* `<head>` import from the [morula project](https://github.com/inriverie/morula/blob/master/_assets/html/partials/html-head.kit)
* [Google Analytics](https://github.com/inriverie/morula/blob/master/_assets/html/partials/google-analytics.kit) snippet from [morula](https://github.com/inriverie/morula).

### Global Kit language variables

The following Kit language variables **must** be edited prior to creating new pages:

* `$site-name` should reflect the name of project.
* More to come…

### Google Analytics ID

Since each project will have a unique GA UA ID, `_ga-id.kit` should be edited on a per project basis. This file also contains the import for GA mentioned above.