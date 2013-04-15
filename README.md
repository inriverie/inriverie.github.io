# vanilla

Starting point for new web projects.

## Structure

High level directory structure:

    README.md
    /assets                     == css, javascript, etc…
      /css
    /models                     == JSON data models.
    /views                      == includes, layouts, etc…
      /includes
      /layouts
    index.html
    /styleguide                 == example of a sub-site

## CSS

`_config.scss` controls the project style settings. Each `[page].scss` file has a dedicated section where these settings can be over-written on a page-by-page basis.

Directory structure:

    /css
      _config.scss
      _vanilla.scss
      /includes                 == global *.scss partials
      /page                     == contains all page stylesheets
        index.css
        /sass
          index.scss
        /[sub-site]             == styleguide and other sub-pages
          /sass
            [sub-site page].scss
          [sub-site page].css

### Page specific stylesheets

At the top of each `[page].scss` file there's a section to re-define variables:

    /*------------------------------------*\
        NAME OF PAGE
    \*------------------------------------*/
    /**
     * Re-define framework and Vanilla variables
     */

The only required import should be `_vanilla.scss`. This imports all default variables, styles, etc… If the page uses any framework objects, import them after `_vanilla.scss`.

    /**
     * Import all of the things...
     */
    @import "../../../vanilla.scss";

Lastly, there's a section dedicated to styles specific to the page.

    /**
     * Custom page styles
     */

## Data Models

The `_models` directory stores all referenceable data. `*.jade` files contain Jade template variables/objects and `*.json` for Javascript data.

    /models
      _site.jade
      /page
        /[sub-site]
          [sub-site page].json

## Templates and Layouts

Global partials are stored in the `include` directory. `Layouts` contains site templates. It should not require a `[sub-site]` directory as templates should be globally referenced.

    /views
      /includes
        _footer.jade
        _head.jade
        _header.jade
        _nav.jade
      index.jade
      /layouts
        default.jade

## Utilities

* [Codekit](http://incident57.com/codekit/) for all the heavy lifting.
* My Codekit framework [Morula](https://github.com/inriverie/morula).
* Stylesheets written in [SASS](http://sass-lang.com/).
* HTML and templating leverages [Jade](http://jade-lang.com/).
