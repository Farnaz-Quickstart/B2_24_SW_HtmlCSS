# HTML basics

## Introduction

### Outline

- What is markup?
- How do Markdown and HTML represent markup?
- Your First HTML Page explanation of doctype, meta etc.

### Guidelines

- Focus on content, not on style!
- Knowing everything is not necessary!
- VS Code: Emmet, "html:5"
    - `mkdir xyz` -> `cd xyz` -> `code .`
    - Clean work environment
- Alternative online environment: https://codesandbox.io/

### Documentation

- https://www.w3schools.com/
- https://devdocs.io/
- https://htmlcheatsheet.com/

### Live Server 

Live Server configuration

## Tags

- Tags: `<tagname> ... </tagname>`

- Headings: `<h1> ... </h1>` (only one)
- Paragraphs: `<p> ... </p>` (block level elements)

- Whitespaces in VS Code and browser    

- VS Code: "lorem50", Alt+Z (text format), 
- VS Code: `p*3`, `(p>lorem5)*3`

- Browser: development tools

- Italic: `<em> ... </em>` - and not `<i> ... </i>`
- Bold: `<strong> ... </strong>` - and not `<b> ... </b>`

## Lists

- `<ul> ... </ul>`, `<ol> ... </ol>`
- `<li> ... </li>`
- VS Code: `ul>li*6`

## Images
- VS Code: `img`
- `<img src="" alt="">` - we don't need to close images
- Relative paths: `src`, `"images/profile.jpg"`, `"./images/profile.jpg"`, `"../images/profile.jpg"`
- URL path (link)
- Accessibility: `alt`
- Size: `width="250" height="300"`. Don't distort the aspect ratio!

## Ids and Links

- Tag ID: e.g. `id="skill-table"`
- In the browser: e.g. `http://127.0.0.1:5500/index.html#skill-table`

- Internal links:
    - Same file: e.g. `<a href="#social-links">Social Media</a>`
    - Another file: e.g. `<a href="./projects.html">My Projects</a>`
    - Another file with an anchor: e.g. <a href="./index.html#social-links">Social Media</a>
    - Image in another project directory: e.g. <a href="./images/profile.jpg">Me</a>

- External links: `<a href="http://www.google.com">Find Me...</a>`

- In new tab: `target="_blank"`

## Block, Inline, Classes

- `<div> ... </div>` - Generic block level tag
- `<span>...</span>` - Generic inline tag
- Computed style -> display -> block or inline
- Question: which elements are block and which are inline?

- `<div id="header"> ... </div>` - Only one instance
- `<div class="article"> ... </div>` - Multiple instances

- VS Code: `div#header`
- VS Code: `div.article`    

## Semantic HTML

- `<article> ... </article>` - Understandable on its own
- `<section> ... </section>` - General section
- `<aside> ... </aside>` - Can be skipped

## Forms 

- Basic input fields, type attribute: e.g.
    - `<button type="submit">Send</button>` or `<input type="submit" value="Send" />`
    - `<input type="text">`
    - `<input type="email">`
    - `<input type="tel">` - Validation: e.g. `pattern="[0-9]{3}-[0-9]{4}"`

- Name, placeholder and require attributes: e.g. `<input type="text" name="name" id="name" placeholder="Your name" required>`

- VS Code: `input[type=submit]`, `input[type=text]`

- e.g. `<form action="." method="GET"> ... </form>` - submit to home page
- e.g. `<form action="" method="GET"> ... </form>` - submit to current page
- e.g. `<form action="contact.html" method="GET"> ... </form>` - submit to particular page

- Line break: `<br>` - Not recommended! -> Solution: later in CSS or layouting with block level elements.

- Label: e.g. `<label for="last_name"> ...<input id="last_name" ...> </label>`
- Alternative method e.g. `<label>Your message: <input type="submit"> </label>`

- `<textarea name="" id="" cols="" rows=""> ... </textarea>`
- 
- `<select name="" id=""> <option value=""> ... </option> ... </select>` - With multiple option tags
- `<fieldset> ... </fieldset>` - Field set
    - `<legend> ... </legend>` - Title of a field set section
- `<input type="radio">` - Multiple radio button with the same name attribute
- `<input type="checkbox">`

- `<input type="range">`

- In developer tools (with get method): `document.location.search.slice(1).split("&")`

## Multimedia

- `<video src=" ... " height="300" autoplay muted></video>`
- `<video> <source src=" ... "> <source src=" ... "> </video>`
- YouTube iframe (frameholder problem)
- `<audio src=" ... " type="audio/mp3" controls></audio>`

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
