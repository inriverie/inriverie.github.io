# Vanilla

Barebones starter files and directory structure for new web projects.

## Build

    mkdir [PROJECT-NAME] && cd [PROJECT-NAME]
    git init
    git remote add inriverie https://github.com/inriverie/[PROJECT-NAME].git
    git remote add vanilla https://github.com/inriverie/vanilla.git
    git pull vanilla master
    git add .
    git commit -m "init"
    git push inriverie HEAD

## Stylesheets

`config.styl` controls the project style settings. New stylesheets should only need to import `config.styl` to inherit framework.

    @import '../config'
    // page or project specific css here
