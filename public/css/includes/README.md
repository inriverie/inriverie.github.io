## `sections.styl`

    /*------------------------------------*\
        HEADINGS
    \*------------------------------------*/
    $hN
      unless display_family == text_family
        font-family display_family
      margin  0


    h1,.alpha
      set-font-size(ms6)
      @extends $hN

    h2,.beta
      set-font-size(ms5)
      @extends $hN

    h3,.gamma
      set-font-size(ms4)
      @extends $hN

    h4,.delta
      set-font-size(ms3)
      @extends $hN

    h5,.epsilon
      set-font-size(ms2)
      @extends $hN

    h6,.zeta
      set-font-size(ms1)
      @extends $hN


    if massive_headings
      .giga
        set-font-size(ms9)
        @extends $hN

      .mega
        set-font-size(ms8)
        @extends $hN

      .kilo
        set-font-size(ms7)
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
      border-bottom   1px solid lighten(link_color, 40%)
      color           link_color
      text-decoration none
      transition      all .25s


      &:hover
        border-bottom-color lighten(link_color, 30%)
        color               darken(link_color, 20%)


      // Improve readability when focused and also mouse hovered in all browsers.
      &:active
        outline:0


      // Address `outline` inconsistency between Chrome and other browsers.
      &:focus
        outline thin dotted




## `forms.styl`

    if use_forms

      /*------------------------------------*\
          FORM
          Address margins set differently among browsers.
      \*------------------------------------*/
      form
        margin 0 // [1]





      /*------------------------------------*\
          FIELDSET
          Define consistent border, margin, and padding.
      \*------------------------------------*/
      fieldset
        border  0
        margin  0
        padding half_rhythm





      /*------------------------------------*\
          LEGEND

          1. Correct `color` not being inherited in IE 8/9.
          2. Remove padding so people aren't caught out if they zero out fieldsets.
      \*------------------------------------*/
      legend
        if legacy_support
          border  0 // [1]
        padding 0 // [2]





      /*------------------------------------*\
          LABEL
          `.additional` e.g. Phone (why ask?)
      \*------------------------------------*/
      label,
      .label
        cursor  pointer
        display     block
        line-height line-height


        .additional
          font-weight normal





      /*------------------------------------*\
          INPUT TEXT
      \*------------------------------------*/
      .input--txt
        // foo bar





      /*------------------------------------*\
          INPUT CHECKBOX and RADIO

          1. Remove excess padding in IE 8/9.
      \*------------------------------------*/
      input[type="checkbox"],
      input[type="radio"]
        margin-right  0.25em

        if legacy_support
          padding     0 // [1]





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
          FORMFIELD

          fieldset
          .form-field
            label
            input.input--txt
          .form-field
            label
            select
      \*------------------------------------*/
      .form-field
        @extends .rhythm-bottom


        &:last-child
          margin-bottom 0





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


      .check-label,
      .check-list label,
      .check-list .label
        display inline-block





      /*------------------------------------*\
          SPOKEN FORM INPUTS

          p.spoken-form
            Hello, my 
            label(for='spoken-name') name
            is
            input#spoken-name.text-input(type='text')
            My home
            label(for='country') country
            is
            select#country
              option UK
              option US
              option Other
      \*------------------------------------*/
      if spoken_word
        .spoken-form label
          display inline-block
          font    inherit





      /*------------------------------------*\
          INPUT HELP

          Extra help text displayed after a field when that field is in focus, e.g.:

          label(for='email') Email
          input#email.text-input(type='email')
          small.extra-help .edu emails only

          We leave the help text in the document flow and merely set it to `visibility:hidden;`. This means that it won’t interfere with anything once it reappears.
      \*------------------------------------*/
      if input_captions
        .extra-help
          display     inline-block
          visibility  hidden

        .input--txt:active + .extra-help,
        .input--txt:focus + .extra-help
          visibility  visibile





    /*------------------------------------*\
        FORM VALIDITY
    \*------------------------------------*/
    if use_forms

      :valid
        // foo bar
      :invalid
        // foo bar


      // Error styles starting from `.form-field`
      .invalid
        // color hsl(0, 50%, 50%)
