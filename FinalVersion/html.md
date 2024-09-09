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