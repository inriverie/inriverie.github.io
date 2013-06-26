# vanilla

Static web project

## CSS

`_config.scss` controls the project style settings. Each `[page].styl` file has a dedicated section where these settings can be over-written on a page-by-page basis.

### Page specific stylesheets

    // Import settings
    @import '_vars'
    @import '../_config'


    // Redefine variables here (see _config)


    // Import all of the things…
    @import '../_vanilla'


    // Custom page styles

## Utilities

* [Codekit](http://incident57.com/codekit/) for all the heavy lifting.
* My Codekit framework [Morula](https://github.com/inriverie/morula).
* CSS preprocessed with [Stylus](http://learnboost.github.io/stylus/).
* Templating with [Jade](http://jade-lang.com/).