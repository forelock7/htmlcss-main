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
- Conceptual Aside: Object - a collection of data(information) and code (that accomplish things) which together represents something
- Conceptual Aside: Models - representation of a thing. Object model - a collection of objects that represents a thing and provide access to examine and change that thing.
- The Document Object Model (DOM) - represents an HTML document, providing the ability to examine and change. This is what the browsers uses to create a visual representation of HTMLL document. DOM Tree
- Building the DOM - User Agent takes HTML document from Server and builds DOM. Blink for example: parser read HTML and create an object (DOM).
- Conceptual Aside: Developer Tools. 
- The Inspector - one of the Dev Tools of browser. We actually see html converted from DOM, but not original html.
- Anchor Tags (again). id - unigue attribute to identify some elements for example to create particular URL: if <section id="skills"> so URL to that section is: http://127.0.0.1:5500/C1_HTML_ADocument/Begin/index.html#skills
Also could be created linked list to sections <li><a href="#aboutme">About Me</a></li>
- Engine Aside: Gecko (Mozilla FireFox)
- Engine Aside: WebKit (Safari)