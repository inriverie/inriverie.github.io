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
