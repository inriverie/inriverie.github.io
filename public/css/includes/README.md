## `sections.styl`

    /*------------------------------------*\
      HEADINGS
    \*------------------------------------*/
    $hN
      margin  0


    .h1
      font-size ms(6)
      line-height()
      @extends $hN

    .h2
      font-size ms(5)
      line-height()
      @extends $hN

    .h3
      font-size ms(4)
      line-height()
      @extends $hN

    .h4
      font-size ms(3)
      line-height()
      @extends $hN

    .h5
      font-size ms(2)
      line-height()
      @extends $hN

    .h6
      font-size ms(1)
      line-height()
      @extends $hN


    if massive_headings
      .giga
        font-size ms(9)
        line-height()
        @extends $hN

      .mega
        font-size ms(8)
        line-height()
        @extends $hN

      .kilo
        font-size ms(7)
        line-height()
        @extends $hN





    /*------------------------------------*\
      STRUCTURE ELEMENTS
    \*------------------------------------*/
    [role="banner"]
      // foo


    [role="main"]
      // foo

    .site-nav
      // foo

    [role="contentinfo"]
      // foo





## `links.styl`

    /*------------------------------------*\
      HYPERLINKS
      csswizardry.com/2011/05/on-negative-hovers
    \*------------------------------------*/
    a
      color           link_color
      text-decoration none
      transition      all .25s


      &:hover
        color               darken(link_color, 12%)


      // Improve readability when focused and also mouse hovered in all browsers.
      &:active
        outline:0


      // Address `outline` inconsistency between Chrome and other browsers.
      &:focus
        outline thin dotted




## `forms.styl`

    if use_forms
      /*------------------------------------*\
        LABEL
        `.additional` e.g. Phone (why ask?)
      \*------------------------------------*/
      label,
      .label
        cursor      pointer
        display     block
        line-height line_height


        .additional
          font-weight normal





      /*------------------------------------*\
        INPUTS
      \*------------------------------------*/
      .input--txt
        width 100%


      input[type="checkbox"],
      input[type="radio"]
        margin-right  0.25em





      /*------------------------------------*\
        SELECT
        Put `select` icon back with dropdown.svg

        1. Prevents Webkit from locking `font-size`.
      \*------------------------------------*/
      select
        -webkit-appearance  button // [1]





      /*------------------------------------*\
        PLACEHOLDER

        1. Chrome, Safari
        2. Firefox 19
        3. IE 10
      \*------------------------------------*/
      ::-webkit-input-placeholder
        // [1]
      ::-moz-placeholder
        // [2]
      :-ms-input-placeholder
        // [3]

      :focus::-webkit-input-placeholder
        // [1]
      :focus::-moz-placeholder
        // [2]
      :focus:-ms-input-placeholder
        // [3]





      /*------------------------------------*\
        CHECKLIST

        ul.check-list
         li
           input
           label
         li
           input
           label
      \*------------------------------------*/
      .check-list
        list-style  none
        margin      0


      .check-list .label
        display inline-block
