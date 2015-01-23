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

## HTML

New HTML documents `extends` `layout.jade` and injects content where needed. Available blocks are: `vars`, `head`, `content`, and `scripts`.

    extends layout
    append head
      meta(name='description', content='Desciption text…')
      title Title text…
      link(rel='stylesheet', href='../assets/css/example.css')


## Stylesheets

Stylesheets only need to import `document.styl`. Import others, i.e. forms.styl, after.

    @import '../document'
    @import '../forms'
    // page or project specific css…
