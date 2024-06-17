# HTML and CSS

This repository is contains the code used in my course "Understanding HTML and CSS". Find the course here: https://www.udemy.com/course/understanding-html-and-css/?referralCode=29ED997A126F1B7FF1DF

# Section 1: Introduction

# Section 2: Trees

-   Trees - data structure which is used in html
-   Traverse - travel across or through (tree)

# Section 3: HTML

-   User Agents: browsers, screen readers, googlebot
-   Tag - a way to markup the document that is friendly to user agents
-   the markuo describe the document
-   by marking up a document you are attempting to add meaning

-   Tags, attributes and element
-   nested elements

-   markup language is everywhere (for instance in zip files)

-   specifications - a standard of precise requirements
-   HTML specofocation: https://html.spec.whatwg.org/multipage/
-   Normative - establishing a standard

-   Authors of documents - developers of web applications
-   Implementors of tools - creators of browser

# Section 4: The Document

-   '<!DOCTYPE html>' - said user agent that this document is standard of HTML
-   'html' - element represents the root of an HTML document

-   Metadata - a set of data that provides information about other data

    -   Alicea - data -> lasttname - metadata
    -   Tony - data -> firstname - metadata

-   'title' element represents the document's title and name
-   Author should use titles that identify their documents even when they are used out of contrext. No more than one title element per document

-   character set - set of supported characters (numbers, letters, symbols). UTF-8 covers almost everything in every language.
-   '<meta charset="UTF-8">' element isn't closed

# Section 5: Document Sections

-   outline - <section></section>
-   self-containd composition - example element <article></articale>
-   Thematic grouping of content - <section></section>
-   Tangential Content - <aside></aside> - aside element represents a section of a page that consists of content
    that is tangentially related to the content around the aside element
-   Heading and rankins - <h1></h1>, <h2></h2> ... <h6></h6> - represents implicatly a new section.
    If following heading with lower ranking - subsection
-   Headers and footers - <header><header>, <footer></footer>
-   Addresses - <address></address>

# Section 6: Grouping Things

-   Paragraphs - <p></p>
-   Quats - <blockquote> - uses outside <p></p>
-   Unordered list <ul><li></li></ul>
-   Odered list <ol reversed><li></li></ol>, where 'reversed' attr represents reversed order
-   Association list - <dl><dt>Title</dt><dd>Value</dd></dl>
-   Multidimennsional Content (Table) <table><thead>....</thead>....</table>, <thead></thead>
    Structure vs Semantic - not always DB data representation should be a html table
-   Dominant Content - <main></main>
-   <div></div> - has no special meaning at all. It represents its children. Do not replace all elements by 'div'!!!

# Section 7: Text Itself

-   emphasis - <em></em> - stress emphasis of text content <p><em>Cats</em> are cute animals</p>.
    Could be display as automaticaly(by user agent - browser): <i></i> - italics element
-   Importance - <strong></strong> - could be used in <h1>.. - Something serious or urgent
-   Side comments - <small></small>
-   Line Breaks - <br /> or <br> - self closing element
-   Author's comments - <!--Needs pectures--> - could be multilines
-   <span></span> similar to div, but for text. Do not overuse it like div. Doesn't mean what it owns. Just represent childrens

# Section 8: The Browser and the DOM

-   Conceptual aside: HTTP - to deliver HTML from server to client (agent) and reverse. Hyper text - beyond text(more than text), hypermedia
-   Anchor Tags and Hypertext - <a href="https://google.com" target="_blank">, <area>, - to link diferent resources. target - browser context (open a new browser context - new tab)
-   Conceptual Aside: User Agents(again) - laptops, tablets - back and forth interaction between user - agent - server
-   Conceptual Aside: the browser. Rendering engine - a computer that transforms an HTML document into visual, interactive representation
-   Blink: A Rendering Engine of chromium
-   Engine Aside: Parsing. - analtze text, charecter by character.
-   Named Character References - '<h1>3<5</h1>' -> '<h1>3&lt;5</h1>' - to convert character into some coded to avoid unexpected behaviour
-   Conceptual Aside: Object - a collection of data(information) and code (that accomplish things) which together represents something
-   Conceptual Aside: Models - representation of a thing. Object model - a collection of objects that represents a thing and provide access to examine and change that thing.
-   The Document Object Model (DOM) - represents an HTML document, providing the ability to examine and change. This is what the browsers uses to create a visual representation of HTMLL document. DOM Tree
-   Building the DOM - User Agent takes HTML document from Server and builds DOM. Blink for example: parser read HTML and create an object (DOM).
-   Conceptual Aside: Developer Tools.
-   The Inspector - one of the Dev Tools of browser. We actually see html converted from DOM, but not original html.
-   Anchor Tags (again). id - unigue attribute to identify some elements for example to create particular URL: if <section id="skills"> so URL to that section is: http://127.0.0.1:5500/C1_HTML_ADocument/Begin/index.html#skills
    Also could be created linked list to sections <li><a href="#aboutme">About Me</a></li>
-   Engine Aside: Gecko (Mozilla FireFox)
-   Engine Aside: WebKit (Safari)

# Section 9: Accessibility

-   Accessibility - ability to be accessed and used independantly by people no matter their circumstances
-   Screen readers - user agent like a browser (not visual way, through speech, brail). It wors better with good semantic of html document
-   ARIA - specification of w3 organization

# Section 10: Interactivity

-   Navigation - <nav></nav> - navigation block
-   Engine Aside: Forms and HTTP. GET /search?q=html&page=3 - querystring after '?'. name/value pairs separated by '&'.
    -   Forms build name/value pairs meant to be sent via HTTP.
-   Forms, Fields and Labels.
    -   <form action="dosomething.html"></form> - represents hyperlink, that can be manipulated (payload).
    -   Attributes for form submission: action, enctype, method, novalidate, target.
    -   There are elements which is associated with form - button, input
    -   Field - html elements allow user to input informations: <input type="text">.
    -   <input type="text" name="name" /> - by name user agent recognise it and suggest autofill
    -   <label for="name"></label><input></input id="name"> - represents a a caption in a user interface. "for" - assosiate label with element where is id the same. Click on associated label is click on input.
-   Buttons
    -   elements to submitting the data
    -   <input type="button" value="Send" /> as a button without any default behaviour (can't have child elements)
    -   <input type="submit" value="Send" /> as a button with submit form
    -   <button type="submit">Send</button>
    -   <form action="dosomething.html"> - send GET http request with name/value querystring (URL params) URL={baseURL}/dosomething.html
    -   <form action="dosomething.html" method="POST"> - send POST http request with name/value payload (Form Data in body)
-   More Fields:
    -   <input required /> - required attribute
    -   <label> and <input> can be wrapped by <p></p>
    -   select ->>> <select id="whycontacting" name="whycontacting"><option value="jobinterview">Job Interview</option>
    -   textarea ->>> <label for="comments">Comments</label><textarea id="comments" name="comments" rows="3"></textarea>
-   Even More Fields:
    -   radiobutton - <p><label for="contacttime2">Afternoon</label><input type="radio" id="contacttime2" name="contacttime" value="afternoon" /></p> - 'name' attr is the same; 'id', 'value' - are different for each variant - name/value pair is 'contacttime=afternoon'
    -   checkbox - <p><label for="asap">ASAP</label><input type="checkbox" id="asap" name="asap" /></p> - name/value pair is 'asap=on' if checked
    -   <fieldset> - to group all radiobuttons and/or checkboxes (uses also <legend> as title for group)

# Section 11: JavaScript Frameworks

-   Conceptual Aside: DOM Manipulation - changing DOM tree after the HTML doc has been parsed and DOM has been created. Usually done manually via JS code. Browser gives JS possibility to manupulate DOM.
-   React, Angular, Vue and HTML Authoring - tools to manupulate DOM. Still use semantic in templates, not overuse <div>

# Section 12: Stylesheets and Querying Trees

-   The CSS Specifications: https://www.w3.org/Style/CSS/
    -   styleshieet - a collection of stylistic rules
    -   CSS Snapshot - version of CSS specofication for a particular time (CSS Snapshot 2021)
-   User Agent Stylsheet - collection of stylistic rules that the user agent follows when display an HTML document
    -   Default CSS in browser -->>>https://chromium.googlesource.com/chromium/src.git/+/refs/heads/main/third_party/blink/renderer/core/html/resources/html.css
    -   https://www.wiumlie.no/2006/phd/
    -   p {font-weight: bold;} - CSS Rule (Ruleset), where 'p' - selector; '{}' - declaration block, stylistic group; 'font-weight' - property; 'bold' - value; 'font-weight: bold' - declaration
-   Selector - pattern that match (find) against elements in tree. 'p' - type selector
-   Declarations - will apply to element found by selector
-   Inheritance - propagates proparties values to their children, values are computed
-   Author Stylesheets: <link rel="stylesheet" href="styles.css" />
-   Universal Selector: \*{} - entire tree, all elements
-   Attribute Selectors. For example
    [class~="resume-list"] {
    font-style: italic;
    }
-   ID Selector: # - h1#someid, #someid:
    #skills {
    font-weight: bold;
    }
-   Class Selector: '.'
    .pastoral {color=green} === class~=pastoral
    h1.pastoral {color=green}
    h1.some-class.second-class - h1 element which has both classes
-   Grouping Selectors - separate by comma ','
    ul, ol {...}
    ul[lang],
    ol.resume-list {
    font-weight: bold;
    }
-   Combinators: Descendant. - separate by space ' '
    ul p {...} - looking 'p' which has 'ul' as a ancestor
-   Combinators: Child - looks for DIRECT child, not only descendants
    body > p {...} - direct child
    div ol>li p {...}
-   Combinators: Next-Sibling - imidiatly sibling element
    ul + p {...}
