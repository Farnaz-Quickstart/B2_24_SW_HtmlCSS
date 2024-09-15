# CSS basics

## CSS selectors

CSS rule:

selector {
    property: value;
    property: value;
    property: value;
}

CSS cheat sheet

- CSS link: `<link rel="stylesheet" href="styles.css">`
- Selectors (precedency rules)
    - Tag: e.g. `body { ... }`,`nav { ... }`
    - Attribute: e.g. `[type=text] { ... }`
    - Class: e.g. `.introdiction { ... }`
    - Id e.g. `#profile { ... }`
    - `!important` - Do not use!

    - Grouping: e.g. `h1, h2 { ... }`

- Overqualification
    - Specifying: e.g. `p.profile-text { ... }` - every "p" element with "profile-text" class
    - Specifying: e.g. `p#profile { ... }`

- Descendant selector
    - Specifying: e.g. `p .profile-text { ... }` - every "profile-text" class element with "p" parent
    - Universal selector: `* { ... }`

- Google fonts: e.g. `<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Gloria%20Hallelujah">`
- Fonts
    - e.g. `font-family: 'Gloria Hallelujah', Georgia, 'Times New Roman', Times, serif;`
    - e.g. `font-family: 'Antic Slab', Arial, Helvetica, sans-serif;`
    - https://fonts.google.com/

- Developer tools, testing

## HTML basics: Text, lists and display

- Text style and align
    - e.g. `text-decoration: underline;`
    - e.g. `font-weight: bold;`
    - e.g. `font-style: italic;`
    - e.g. `text-align: right;`
    - e.g. `text-align: left;`
    - e.g. `text-align: center;`
    - e.g. `text-align: justify;`

- Lists
    - e.g. `list-style-type: disc;` placed on the ul element
    - e.g. `list-style-type: square;` placed on the ul element
    - `list-style: none;` on the ul element to remove list styles
    - https://devdocs.io/

- Display modes
    - `block` elements
    - `inline` elements
    - `inline-block` elements
    - `flex` elements (Flexbox)


## Units

- Absolute
    - `px`
- Relative
    - `em` Relative to the font-size of the parent element
    - `rem` Relative to font-size of the root element (better way)
    - `vw` Relative to 1% of the width of the viewport
    - `vh` Relative to 1% of the height of the viewport
    - `%` Relative to the parent element
- `calc()` - works with different units


## Box model

- Element
- Padding
- Border
- Margin

- Background color (completely includes the border)

- margin: top right bottom left -> margin: 0, 0, 0, 0
- margin: top left-right bottom -> margin: 0, 0, 0
- margin: top-bottom left-right -> margin: 0, 0
- margin: all -> margin: 0

## Background

- e.g. `background-image: url(../images/background.jpg);`
- e.g. `background-size: cover;` (or contain)
- e.g. `background-position: center center;`
- e.g. `background-repeat: no-repeat;`
- e.g. `background-attachment: fixed;`