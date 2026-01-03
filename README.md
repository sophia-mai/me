# Portfolio Page

Following tutorials:

- https://www.youtube.com/watch?v=0YFrGy_mzjY (JS)
- https://www.youtube.com/watch?v=d56mG7DezGs (TS)
- freeCodeCamp's HTML, CSS and JavaScript Course
- LinkedIn Learning

Tip: Should learn JavaScript first

HTML:

- Hypertext Markup Language, is a markup language for creating web pages.
- headings, paragraph elements
- usually has opening tag and a closing tag
- For content and structure

  Attributes: - value placed inside of opening tag of HTML element
  Basic syntax: - `<element attribute="value"></element>` - the attribute name is followed by an equal sign(=) and a value in quotes.
  Example: Links (anchor element) - `<a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">Visit Video</a>` - without href attribute, link would not work - target="\_blank" opens in new browser tab
  Example: Images - `<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" alt="two cats" />"`
  Example: Checkboxes - `<input type="checkbox" checked />` - checked attribute shows that checkbox is checked. if not there will be unchecked
  Example: input - `<input type="text" disabled>` - disabled doesn't allow for text inputs, not present allows
  Figure: `<figure>...<figcaption></figcaption></figure>`
  Emphasis: italisizes what you wrap around `<em></em>`
  Strong: bolds text `<strong>...</strong>`
  Footer: end of a document typically with copyright info, links to terms, contact info, etc. `<footer></footer>`

  Link Element: - used to link external resources like stylesheets and site icons - `<link rel="stylesheet" href="./styles.css">` - rel attribute used to specify the relationship b/w linked resource and HTML document - href att used to specify location of URL - ./ looks in current directory - best practice to seperate HTML and CSS in diff files - devs use link element for external CSS file instead of writing in HTML document - link element should be placed inside the head element - ex.

            ```<head>
                <meta charset="UTF-8" />
                <meta name="viewport" content="width=device-width, initial-scale=1.0" />
                <title>Examples of the link element</title>
                <link rel="stylesheet" href="./styles.css" />
            </head>```

        - Example Icons:
            - ```<link rel="icon" href="favicon.ico" />```
                - favicon is small icon used to display in browser tab next to site title

  HTML Boilerplate: - template/foundation for webpages

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta
       name="viewport"
       content="width=device-width, initial-scale=1.0" />
    <title>freeCodeCamp</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
    <h1>I am a main title</h1>
    <p>Example paragraph text</p>
  </body>
</html>
```

        - DOCTYPE tells browser which version of HTML
        - html tag wrap around all content
            - tag lang specifies the language of page
                - ```<html lang="en">```
            - inside html tag, two main sections
                - head
                    - important metadata goes inside
                        - meta elements has details about character encoding, site's title
                        - external stylesheets
                - body
                    - where all content goes

    What is UTF-8 Character Encoding?
        - USC Transformation Format 8 is standardized character encoding used on the web
        - encoding: method to store characters as data, bytes
        ```<meta charset ="UTF-8" />```
        - For each new project, should include this meta element with charset to UTF-8

    Div Elements:
        - div is used as a container to group other elements
        - Mainly use div element to group HTML that will share a set of CSS styles
        - don't use divs too much, sometimes section might be better
        - Sections have semantic meaning and websites will treat as a section
        - divs have no semantic meaning

    IDs and Classes:
        - id attribute: adds unique identifier to an HTML element
            - in CSS, the id can be used to reference the HTML element to change how it looks
            - id values can't have spaces in them and should always be unique
            - ex. ```<h1 id="title">Movie Review Page</h1>```
        - class attribute: does not need to be unique and can have spaces
            - You can have multiple classes in an element by separating the names by a space
            - ex. one class: ```<div class="box"></div>```
            - ex. two classes: ```<div class="box red-box"></div>```

    HTML Entities:
        - an HTML entity is a set of characters used to represent a reserved character in HTML
        - Problem: trying to display text and have an ```<img/>``` inbetween some text --> doesn't show desired result bc the ```<``` and ```>``` indicate the beginning and the end of and HTML element
        - Fix: Use entities
        - Ex. ```&lt;p&gt;learning is fun&lt;/p&gt;``` will display &lt;p&gt;learning is fun&lt;/p&gt; with less than and greater than sign
            - Called named character references
        - Named character references:
            - start with an ampersand sign and end with a semicolon
            - by using these, HTML parser doesn't confuse an actual HTML element
            - ex. &lt;
        - Decimal numeric reference:
            - starts with an ampersand (&) and a hash symbol (#) followed by one or more deciml digits followed by a semicolon
                - ex. ```&#169;``` for the copyright symbol and ```&#174;``` for the trademark symbol
        - Hexadecimal numberic reference:
            - starts with an ampersand, hash, and the letter x, then followed by one or more ASCII hex digits and ends with a semicolon
                - ex. ```&#x20AC;``` for the euro symbol and ```&#x03A9;``` for the Greek capital letter Omega symbol

    Role of the Script Element in HTML:
        - script elements: used to embed executable code
            - most will use for executing JavaScript code to add interactivity to web pages
            - best practice to link JavaScript code to an external JavaScript file instead
                - ex of link to external JavaScript file: ```<script src="path-to-javascript-file.js"></script>```
                    - src attribute used to specify location for external JavaScript file

    Role of Meta Descriptions, SEO:
        - Search engine Optimization: practice that optimizes web pages so they become more visible and rank higher on search engines
        - One way to improve SEO is providing a short description for web page using meta element
        ex. ```<meta
                name="description"
                content="Discover expert tips and techniques for gardening in small spaces, choosing the right plants, and maintaining a thriving garden."
                />```
                    - by setting name attribute to description, ensures browsers and search engines know about this type of metadata
                    - the content attribute is where you place the description
                    - recommended that you keep your descriptions short and concise
                    - meta description will not be visible on web page
                        - can befound in its search engine result page snippet

    Role of Open Graph Tags, SEO:
        - open graph protocol enables control on website's content that appears across various social media platforms, ex. LinkedIn
            - by setting these open graph properties, you can entice users to want to click and engage with content
        - set using meta elements inside HTML head section
        - First important OG property to include would be title
            - ex. ```<meta content="freeCodeCamp.org" property="og:title" />```
        - Next important OG property is type
            - ex. ```<meta property="og:type" content="website" />```
                - the type property is used to represent the type of content being shared ex. articles, websites, video, music
        - Third important OG property is image
            - ex. ```<meta
                content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
                property="og:image"
                />```
        - Fourth important OG property is url
            - ex. ```<meta property="og:url" content="https://www.freecodecamp.org" />```

    Role of HTML Audio and Video Elements:
        - audio and video elements allow you to add sound and video content to HTML docs
        - audio supports popular audio formats like mp3
        - video support ex mp4
        - to include audio content on web page can use audio element with src attribute
            - ex. ```<audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/cruising-for-a-musing.mp3"></audio>```
                - to add controls, add controls attribute
                    - ex. ```<audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/cruising-for-a-musing.mp3" controls></audio>```
        - controls is boolean attribute
        - other attributes as well:
            - loop (boolean makes audio replay)
            - muted (boolean when audio element is present, automatically start muted)
        - with audio, dufferences in types that are allowed in browsers
            - solution: use source elements insude audio element and browser selects the first source it understands
                - ex. ```<audio controls>
                    <source src="audio.ogg" type="audio/ogg" />
                    <source src="audio.wav" type="audio/wav" />
                    <source src="audio.mp3" type="audio/mpeg" />
                    </audio>```
            - (all attributes also work with video)
        - video:
            - add autoplay att to opening video tag so video plays automatically
            - add poster att if you want to display an image while video is downloading




CSS:

- For styling

JavaScript:

- helps merge HTML and CSS together
- for interactivity to websites
- what a lot of modern websites use
- has different flavors like TypeScript, CoffeeScript

Steps (JS):

- create index.html
  - type ! and click enter for html template

Tips (JS):

- Use Live Server on VSCode
  - Go to index.html
  - right click the text and click Open with Liver Server
    - Updates website live
- Extensions:
  - ESLint
  - Prettier
- In a website on a browser
  - Inspect > Console > Type window.document
  - You can open the dropdowns to see the HTML

What is TypeScript:

- Built on top of JavaScript
- Is a statically typed language (JS is not)

Steps (TS): - Install Node.js - run in terminal: npm i -g typescript - this installs TS in all folders - create a index.ts file

    Configuring TypeScript Compiler:
        - tsc --init
            - creates tsconfig.json
        - create src and dist folders
        - in tsconfig.json
            - uncomment rootDir to go to ./src
            - uncomment outDir to go to ./dist

Tips for TS:

- running: tsc in terminal compiles all .ts files
- Debugging:
  - in tsconfig.json, have sourceMap to true
  - insert break points in code to start debugging
  - go to debug panel (in VSCode)
  - Click create a launch.json file
    - Select Node.js
  - in launch.json under "program"
    - add "preLaunchTask": "tsc: build - tsconfig.json",
      - tells compiler to use tsconfig.json
  - Now can debug!
    - go to debug panel, at top click "Launch Program"
    - In watch tab, you can add a variable to watch
    - step over goes to next line
    - step into goes into a function
    - step out goes out of a function
