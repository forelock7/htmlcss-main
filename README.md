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
-   Combinators: Next-Sibling - immediatly sibling element
    ul + p {...}
-   Combinators: Subsequent Sibling - all 'p' elements which are sibling to 'h2'
    h2 ~ p {...}

-   Conceptual Aside: CSS Standards and Drafts. https://drafts.csswg.org/
    Each Specification has status:

    -   First Public Working Draft (FPWD)
    -   Working Draft (WD)
    -   Candidate Recomendation (CR)
    -   Candidate Recomendation Draft (CRD)
    -   Proposed Recomendation (PR)
    -   Recomendation (REC)
    -   Superseded Recomendation (SPSD)

-   Browser Support (caniuse and MDN)

    -   https://caniuse.com/
    -   https://developer.mozilla.org

-   Child-Indexed Pseudo-classes.

    -   Pseudo - something is not real.
    -   Pseudo-class - selection based on information that lies outside the document tree
    -   li:nth-child(2n+1) {...} - get all <li> elements devide them into groups by 2 elements and select first. It's the same as li:nth-child(odd) {...}, or 2n+2 === even

-   Typed Child-Indexed Pseudo-classes (and Debugging a Problem) - :nth-of-type
    there is a key difference between :nth-child and :nth-of-type. The :nth-child pseudo-class selects elements based on their position among all children of their parent, regardless of type, while :nth-of-type selects elements based on their position among siblings of the same type.

    -   :nth-child - all children
    -   :nth-of-type - only children with particular type(tag)
    <aside> can't be inside <p>, if you put it, browser can change DOM regarding rules - move <aside> from <p>

-   User Action Pseudo-classes. Locations pseudo-classes:

    -   a:visited { color: red;} - color visited link to red color

-   Input Pseudo-classes.
    a:focus, a:hover { color: red;}
    input:focus {outline: 2px solid black;} - color input border if click inside

-   Negation Pseudo-class:
    section:not(#testimonials) {
    font-style: italic;
    }
    p:not(.no-highlight) {
    font-style: italic;
    }

-   Pseudo-elements - represent abstract elementsbeyond those elements explicitly created by document language. Marked as "::"
    p::first-letter {
    font-weight: bold;
    }

-   The Cascade - applying different styles to the same elements with an ordered list. So it's the process of combining several style sheets and resolving the conficts between them. Resolving is in desceeding order of declarations ("font-style: italic;")

    1. Origin & Impornance
    2. Specificity
    3. Order of appearance

-   Origin from highest priority to lowest:

    1. Important user agent declaration (font-weight: bold !important;)
    2. Important user declaration (when user/readers can change style) - could be ignore for now
    3. Important author declaration
    4. Normal author declaration
    5. Normal user declaration - ignored for now
    6. Normal user agent declaration

-   Importance in CSS declarations (font-weight: bold !important;). Ussually it isn't used. Can be considered if:

    -   you don't have much control over CSS (CSS is used by someone else)
    -   something has gone very wrong

-   Specificity (you can see these numbers in IDE just hovering selector)

    1. count the number of ID selectors in selectors
    2. count the number of class selectors, attributes selectors and pseudo-classes in the selectors
    3. count the number of type selectors and pseudo-elements in the selector
    4. ignore the universal selector
       #skills .resume-list (110) --- win
       #skills (100)
       sections.skills (011)
       .skills (010)

-   Order of Appearance. Last wins:
    <head>
    <link rel="stylesheet" href="styles.css" />
    <style>
    ul {
    font-weight: bold !important;
    }
    </style>
    <link rel="stylesheet" href="styles2.css" /> ---- WIN

-   Cascade Layers and @import - allows to import styles rules

    -   import
        in index.html file:
        <link rel="stylesheet" href="style.css" />
        in style.css file (must be at the beggining of the css file!!!):
        @import "styles.css";
        @import "styles2.css";

    -   layers
        in styles.css:
        @layer default {
        p {max-width: 70ch;}
        }
        in styles2.css:
        @import url(styles.css) layer(default);

-   inherit, initial, and Specified Values
    promarties has two related property. For instance 'font-wigth': Initial: normal; Inherited: yes (https://www.w3.org/TR/css-fonts-4/)
    initial value is normal:
    li {
    font-weight: initial;
    }
    'li' will be bold from 'ul'
    ul {font-weight: bold;}
    li {font-weight: inherit;}
    Specified value - value that is specified directly in declaration

-   Matches-Any Pseudo-Class: ':is()'
    initial:
    ul.resume-list li, ol li {}
    after:
    :is(ul.resume-list, ol) li {}

-   Specificity-Adjustment Pseudo-Class - ':where()'
    Example to fix next:
    a:not(:hover) {text-decoration: none;}
    nav a {/_ Has no effect _/ text-decoration: underline;}
    Fix:
    a:where(:not(:hover)) {text-decoration: none;}
    nav a {text-decoration: underline;}

-   Optimization:
    ul _ {} - user agent seeking element from right to left by selector (find '_' (all elements) and then find parent 'ul') - BAD
    selection p.name {}
    #skills {}

-   Engine Aside: The CSSOM.

# Section 13: Box Model

-   Conceptual Aside: Rendering.
    Inside user agent DOM tree and CSSOM are combined into render tree (Render Tree Construction)
    After having Render Tree user agent do 2 steps of whole Rendering process:

    -   decide whe the all content go (Layout)
    -   displaying the content (Painting)

-   Visual formatting model - the approach taken to render a document tree for visual media
-   Media a means of communication

-   Box Model - visual formatting model of CSS. All elements draw boxes
-   Viewport and Coordinates - part of content which is displayed
-   Layout - calculation according to Box Model
-   Device pixel - the smallest controllable element on a device screen.
-   Pixel Density - the number of physical pixels on a device screen per unit of length (for example, inches)
-   Reference pixels - used by CSS (ipx = 1/96 inch)

-   Units and Computed Values: - Absolute: px, pt - Relative: 2em (increase value in 2 times)
    body {font-size: 6px} - parent element
    section {font-size: 2em} === 12px - taken from parent element('Styles' tab shows 'em' as user agent styles, but 'Computed' tab - 'px')
    ul {font-size: 3rem} - taken from root element
    vw - percentage of view ports

    -   Declared Values
        -   cascading
    -   Cascaded Value
        -   defaulting ( initial, inharitance)
    -   Specified Value
        -   resolving (relative values)
    -   Computed Value
        -   calculating
    -   Used Value
        -   final layout adjustments
    -   Actual Value

-   In 'Computed' tab we have actual values after all stages above

-   Engine Aside: Intrinsic Size - the size (heigh and width) calculated based on content, not on size explicitly specified

    -   min-content
    -   max-content

-   Box Sizing:

    -   Content
    -   Border (around the content)
    -   Padding (box between content and border)
    -   Marging (box between border and other boxes)

    body {font-size: 16px}
    padding-top: 0.5rem; - top=8px
    padding-right: 0.5rem; - right=8px
    ...
    padding: 0.5rem 0.5rem 0.5rem 0.5rem; - top=bottom=left=right=8px
    padding: 0.5rem; - top=bottom=left=right=8px
    padding: 0 0.5rem - top=bottom=0 left=right=8px

-   re-setting - change default user agent styles by your own

    -   \* {box-sizing: content-box;} - by default in user agent
    -   \* {box-sizing: border-box;} - heigh and width is calculated including padding and border
    -   min-width: 700px - could be more, but not less 700px
    -   overflow: hidden; - if content is out of the box, that part of content would be hidden
    -   overflow: auto; - Be Careful in usage of 'auto' value because it means different for different properties.

-   Conceptual Aside: Functions - a map of inputs to outputs. CSS is declaritive language.
-   Calc, min, max, clamp:

    -   max-marging: calc(800px - 2rem)
    -   max-marging: min(700px, 80%, 2rem)
    -   max-marging: clamp(700px, 80%, 2rem) - from min value to max

-   Engine Aside: Formatting Contexts:
    -   Block Formatting context
    -   Inline Formatting context
    -   It's all normal flow

# Section 14: Box Position

-   Positioning Schemes. CSS relies on coordinate-based and offsetting schemes. It can move around elements in ways that can make them overlap other content:

    -   div {position: static} - initial value

-   Static - laid out as expected according to the calculations for particular formatting context (block/inline)
-   Relative -the blox is laid out as static, then offset(move) from its position (work with top/bottom/left/right properties)
    div {position: relative; top: 50px;}
-   Absolute - laid out outside the normal flow of boxes. It's placed to its nearest non-static ancestor. It does not participate in its parent's formatting context
    div {position: absolute; top: 50px;} - it will offset <html> root element (initial containing block) if all other elemnts have default 'static' position
-   Fixed - laid out outside the normal flow of boxes. Its containing block is the viewport.
    div {position: fixed; top: 50px;}
-   Sticky - laid out as relative to its nearestscrolable ancestor
    nav {position: sticky; top: 0;}

# Section 15: Painting and Images

-   The result what we see in the browser:
    -   Loading
    -   Scripting
    -   Rendering
    -   Painting
    -   System
    -   Idle
-   Visibility
    div {visibility: hidden} - element laid out, but paiting skipped.
-   Z-Index:

    -   https://www.w3.org/TR/CSS22/visuren.html#z-index
    -   https://www.w3.org/TR/CSS2/zindex.html
    -   when elements behind or on the top of the othe elements. So they have order of position by Z-axe
    -   Stacking context - order of painting the elements relativly to other
    -   Element in html doc create the new stacking context for children
    -   div {isolation: isolate} - to establish its own islotade stacking context

-   Images: img
    -   https://picsum.photos/ - one of the image placeholder services
    -   images - replaced element
    -   <img src="https://picsum.photos/id/165/200/300" alt="I'd love to be here" />
    -   <img src="./images/myImage.png" alt="I'd love to be here" />
    -   alt - appropriate aternative text of the image

# Section 16: Flow

-   Display: Inner and outer of element in layout

-   Block
    display: block;
    .block2 {marging-bottom: 30px;}
    .block3 {marging-top: 20px;}
-   the space between 2 boxes will be 30px, not 50 becouse of overlaping

-   Float - put element aside content

    -   text will be on the right of image
        <img src="images/man.png" class="my-picture" />
        .my-picture {
        float: left;
        max-width: 75px;
        margin-right: 1rem;
        }
    -   if use clear property:
        img {clear: both} - there is no any content aside of image
    -   Floated element could be outside parent element box

-   Inline, Vertical Align, Line-Height and More.

    -   inline - formatting context, boxes are laid out horizontally. Horizontal marging, borders and padding are respected between these boxes.
        display: inline;
    -   line-heigh: 5px - heigh of text line inside element, not all box
    -   text-alighn: center; - align of text line inside of elements
    -   Midified a list of titles:
        nav ul li {
        display: inline;
        margin: 0 0.25rem;
        line-height: 1.5rem;
        }

-   flow-root and BFCs - To overcome overlaping of image inside box (parent element) use 'flow-root', instead of inherited 'blox':
    #aboutme {
    ...
    display: flow-root;
    }

-   Writing Mode:

    -   Commonly 'Inline' (from left to right) and 'Block' (from top to bottom)
        body {writing-mode: vertical-rl;} - right to left
        body {writing-mode: horisontal-bt;} -from bottom to top
    -   marging and padding properties are not multi lang, so wrighting mode is not applied to those properties

-   Direction:
    body {direction: rtl;}

-   Text-Orientation
    body {text-orientation: upright;}

-   Logical Properties.

    -   Usage of next properties is better than padding-marging in multi lang representation:
        -inline-start, -inline-end (inline-size), -block-start, -block-end(block-size)
        Example: marging-inline-start
    -   Instead margin: 0 0.25rem;
        Use:
        margin-inline: .25rem;
        margin-block: 0;
    -   Instead max-width: clamp(700px, 50%, 900px);
        max-inline-size: clamp(700px, 50%, 900px);
    -   /_ padding: 0 2rem; _/
        padding-inline: 2rem;
        padding-block: 0;
    -   /_ border-left: solid 2px black; _/
        border-inline-start: solid 2px black;
        /_ border-right: solid 2px black; _/
        border-inline-end: solid 2px black;
    -   /_ border: solid 1px black; _/
        border-inline: solid 1px black;
        border-block: solid 1px black;
    -   /_ margin-bottom: 1.25rem; _/
        margin-block-end: 1.25rem;
    -   /_ float: left; _/
        float: inline-start;
    -   /_ max-width: 75px; _/
        max-inline-size: 75px;

-   Sticky Nav Note:
    /_ inset-inline-start: 0; _/ - somehow it doesn't work
    top: 0;

-   Inline-Block
    body {display: inline-block;} - element has its own flow in this way

-   None
    body {display: none} - never laid out (excluded from the render tree)
    hidden - laid pout, but not painted. none - not laid out at all
    <title>, <head> - display: none;

-   Table, List-Item, and More

# Section 17: Flexbox

-   Flex Formatting Context. In flex layout we have new axes:

    -   Main (in block layout - inline)
    -   Cross (in block layout - block)

-   There is no need a writting mode to multi lang
    div {display: flex;} - div is block, but its direct children are flex items

-   Flow Direction.

    -   flex-direction: row; - like inline, horizontaly
    -   flex-direction: row-reverse;
    -   flex-direction: column; - like block, vertical
    -   flex-direction: column-reverse;

-   Display Order.

    -   Example 1:
        #aboutme {display: flex;}
        #aboutme aside {order: 10;} - <aside> element is not last sibling in #aboutme, but will be displayd as a last
    -   Example 2:
        #testimonials {display: flex;flex-direction: row-reverse;}
        #testimonials h2 {order: -2;} - first in order (from right)
        blockquote.featured {order: -1;} - second in order (from right)

-   Wrapping and Overflow
    #aboutme {display: flex; overflow: hidden;} - flex item will not overlap the blox container(overlaped part is not visible)
    #aboutme {display: flex; overflow: scroll;} - flex item will not overlap the blox container(overlaped part is not visible), but scrollbar appears
    #aboutme {display: flex; overflow: auto;} - if needed scroll bar appears
    nav ul {display: flex; flex-wrap: wrap;} - new flex line is created if items can't be placed

-   Flex:

        -   Flex box -> | flex item 1 | flex item 2 | flex item 3 | positive free space |
        -   flexItem {flex-grow: 1;} - if all items have the same value, positive free space will be split equally with proportions and extend all items
        -   flex-grow: 0; - isn't extended with free space

        -   Flex box -> | flex item 1 | flex item 2 | flex i... negative free space |
        -   flexItem {flex-shrink: 1;} - if all items have the same value, negative free space will be split equally with proportions and shrink all items
        -   flex-shrink: 0; - item isn't shrinked

        -   flexItem {flex-basis: 50%;} - we can garantee that item will not extended and combining with flex-shrink: 0; not shrinked
        - .flex-header, .motto {flex-basis: 100%;}
        - flex-basis: auto - based on content

        - item {flex: 1 30%} - flex-grow and flex-basis
        - item {flex: 1 2} - flex-grow and flex-shrink
        - item {flex: 1 2 auto} - flex-grow, flex-shrink and flex-basis

-   Alignment.

    -   {justify-content: flex-start;} - initial value - align items to the left
    -   {justify-content: flex-end;} - align items to the right
    -   {justify-content: flex-center;} - align items to the center
    -   {justify-content: space-between;} - distribute items on the line equally
    -   {justify-content: space-around;} - the same as 'space-between', but gives more space at the beginning and at the end

    -   alighn-content: stretch - distribute content in lines equaly in the box
    -   align-item: flex-start (to all items) - what to do with 'cross' space direction (bottom)
    -   align-self: flex-start (to particular items) - what to do with 'cross' space direction (bottom)
    -   : baseline - alighn to the bottom of the characters

-   Collapse.

    -   it doesn't behave in browser as in spec

-   Inline-Flex
    -   {display: inline-box} - Compared to display: inline, the major difference is that display: inline-block allows to set a width and height on the element.

# Section 18: Grid

-   Grid Formatting Context - display: grid;

    -   Grid enforces 2-dimensional alignment, uses a top-down approach to layout
    -   Flexbox focuses on space distribution within an axis, uses a simpler bottom-up approach to layout

    -   Grid lines(always there is one on the left, second need specify) -> '|' inside is 'Column'('Track').
        Second line specify by size to it from first line
    -   Row(track)
    -   Intersection of horizontal and vertical lines - 'Grid Cell'

-   Conceptual Aside: Fractional Units

-   Track Sizing. -
    #portfolio {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr; - specify 4 colums
    grid-template-rows: 1fr 1fr; - 2 rows
    grid-gap: 10px; - width of grid line
    }
    #portfolio img {
    max-inline-size: 100%; - to make grid cells with the same size (avoid overlaping/extending cells by image content)
    }

    -   repeat() function:
        grid-template-columns: repeat(4, 1fr); - 4 colums
        grid-template-rows: repeat(2, 1fr); - 2 rows
    -   grid-template: repeat(2, 1fr) / repeat(4, 1fr); - 2rows and 4 columns

-   Item Placement

    -   img.anchor {grid-row-start: 2; grid-column-start: 3;} - move image into 2 row and column 3
    -   grid-column-end: 5 - overlaping into column 4
    -   grid-column 3/5; === grid-column-start: 3; grid-column-end: 5;
    -   grid-area: 1 / 3 / 3 / 5 ==== grid-row-start: 1; grid-row-end: 3; grid-column-start: 3; grid-column-end: 5
    -   grid-row: 1 / span 2 === grid-row-start: 1; grid-row-end: 3;

    -   placing items into grid by name:
        #portfolio {
        display: grid;
        grid-template: repeat(2, 1fr) / repeat(5, 1fr);
        grid-template-areas:
        "portfolio anchor img1 img2 img3"
        "portfolio anchor img4 img5 img6";
        grid-gap: 10px;
        }
        #portfolio h2 {
        grid-area: portfolio;
        }
        img.anchor {
        grid-area: anchor;
        }

-   Track Repetition - space-sensitive track repetition and automatic addition of rows or columns to accommodate additional content:

    -   if needed browser engine create rows implicitly. To
        grid-auto-rows: 150px; - give them size we can specify it
        grid-auto-flow: column; - will be created not row, but columns

-   Alignment and Spacing
    align-content
    justify-content
    align-items
    justify-items

    -   Example:
        #portfolio {
        ....
        align-items: end;
        }
        #portfolio h2 {
        grid-area: portfolio;
        align-self: start;
        }
        img.anchor {
        grid-area: anchor;
        align-self: start;
        }

-   Layering - ability to overlap content and control layering with z-index
    grid-row: 1;
    grid-column: 4;
    z-index: 1; - to overlap other content in the same grid cell

-   A Visual Change - put all content into the center of gid (2 column of 3)
    main {
    padding-block: 0;
    margin-block: 0;
    display: grid;
    grid-template-columns: 50px 1fr 50px; - define 2, 3 and 4 grid lines (first is default)
    }
    main > \* {
    grid-column: 2; - start from 2 grid line
    }

        - extend one row tofrom 2 column to 1 and 3:
        .full-bleed {
        grid-column: 1 / span 3;
        padding-inline: 2rem;

    }

# Section 19: Fonts, Colors and More

-   Fonts

    -   h1,h2 {font-family: Arial, Helvetica, sans-serif;} - font families in order of availibility in browser
    -   Google fonts: https://fonts.google.com/selection/embed
        -   add links to the head of html:
        <link rel="preconnect" href="https://fonts.googleapis.com" />
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
        <link
            href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap"
            rel="stylesheet"
        />
        -   add css styles:
            font-family: "Montserrat", sans-serif;
    -   text-transform: uppercase;

-   Hexadecimal, RBG, and Named Colors

    -   RGB - combinations of Red, Green, Blue
    -   Decimal(10) representation - rgb(247, 77, 101)
    -   Hexidecimal(16) representation - #f74d65

    -   background-color: black; - background color
    -   color: white; - text color

-   Opacity - see-though - is oposite to transparency

    -   background-color: rgb(247, 77, 101, 0.9); - 0.9 is opacity property
    -   opacity could be applied to any element:
        #portfolio img:hover {opacity: 0.7; }

-   Backgrounds:

    -   div {
        background-image: url(images/unsplash_background.jpg);
        background-size: cover;
        color: white;
        }

-   Transitions - allows property changes in CSS values to occur smoothly over a specified duration - transition-property, tarnsition-... - #portfolio img:hover {opacity: 0.7;transition: opacity 1s;} - ease - curve how transition happens:
    #portfolio img:hover {opacity: 0.7;transition: opacity 1s ease-out;} // liniar, etc - more example:
    .button {
    background-color: #000000;
    color: white;
    font-family: "Montserrat", sans-serif;
    }
    .button:hover {
    background-color: rgb(247, 77, 101, 0.9);
    transition: background-color 0.5s;
    }

-   Animations - keyframes (https://animate.style/, https://github.com/animate-css/animate.css)

    -   Example (https://github.com/animate-css/animate.css/blob/main/source/fading_entrances/fadeInUp.css):
        @keyframes fadeInUp {
        //// start
        from {
        opacity: 0;
        transform: translate3d(0, 100%, 0);
        }
        //// finish
        to {
        opacity: 1;
        transform: translate3d(0, 0, 0);
        }
        }
        //// class to use in code
        .fadeInUp {
        animation-name: fadeInUp;
        }
    -   Use by adding link to head from (https://animate.style/)
    <head>
    <link
        rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
    />
    </head>
    -   use class from docs:
    <h1 class="animate__animated animate__fadeInUp">An animated element</h1>

-   Images: SVGs - drawings - it's a scaleable image which is drawn by browser, just give an instructions

    -   download svg file and refer in html to it:
        <dt><img src="images/twitter.svg" class="social_logo" />Twitter</dt>
        .social_logo { inline-size: 1rem;}
    -   <svg> element could be directly put into html

-   A Semantic Change

-   Visual Design and User Experience
    -   <footer><a href="#contactme">Contact me</a></footer>
    -

# Section 20: Responsiveness and Querying Media

-   Media - means by which something is comunicaed or expressed (a screen, paper, spoken, with a braille device, etc)

-   Media Queries - '@media ... {...}'

    -   By default CSS rules has media="all":
          <link rel="stylesheet" href="styles.css" media="all" />
    -   Other values: madia="print"
    -   Also some specific rules could be applied:
        @media {...}

-   Viewports and Zoom:

    -   When you need to treat viewport according to actual width (when use phone or tablet instead of laptop):
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    -   "width=device-width" - intend viewport to be the actual width of device
    -   "initial-scale=1" - don't zoom up

-   Media Features

    -   @media screen and (max-width: 767.98px) {} - apply certain rules if scren width equal or less 767.98px (breakpoint)
    -   @media screen and (min-width: 1200px) {} - apply certain rules if scren width equal or more

-   Media Query Range Syntax

    -   @media screen and (767.98px < width <1200px) {}
    -   @media screen and (max-width: 767.98px) === @media screen and (width <=767.98px)

-   Mobile First - approach when you create styles for mobile initialy and then via media adjust it for bigger screens

-   Images: srcset and picture

    -   https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images
    -   Display particular images (with resolutions) for particular media queries:
        <img srcset="elva-fairy-480w.jpg 480w, elva-fairy-800w.jpg 800w"
        sizes="(max-width: 600px) 480px, 800px"
        src="elva-fairy-800w.jpg"
        alt="Elva dressed as a fairy" />

-   Print - change something for printing of site:
    @media print {
    #aboutme {background-color: white;color: black;}
    #contactme {display: none;}
    }

# Section 21: Saving Time and Effort

-   Custom Properties for Cascading Variables
    #aboutme {
    ...
    --test-color: blue;
    }
    #aboutme aside {
    ...
    color: var(--test-color, red);
    } - Where:
    --test-color - custom property
    color: var(--test-color, red); - usage of custom property as var. 'red' is applied if '--test-color' doesn't exist. Custom properties is applied only in inherited elements!!!

    -   To use custom property everywhere use ':root' pseudo class:
        :root {--accent-color: rgb(247, 77, 101, 0.9);}

-   Minification - remove extra characters from document as possible

    -   There are extantion to minify files, shrink the text, like all css file text in one line.
    -   Then use this file in html instead of initial:
    <link rel="stylesheet" href="styles.min.css" media="all" />

-   HTML Validation
    -   https://validator.w3.org/
    -   Validate your HTML, check the errors

# Section 22: CSS Frameworks

-   Being Better Than Frameworks:
    -   Bootstrap (lot of div/span, there is mno semantic choice), usage only predefined classes
    -   Tailwind - semantic a bit better (not only div/span)

# Section 23: Game Changing CSS

-   Next is game changing CSS

# Section 24: CSS Nesting

-   208. The Nesting Module - allows related styles place in one structure
         .foo {
         color: red;
         }
         .foo .bar {
         font-size: 1.4rem;
         }

    ***

    .foo {
    color: red;
    .foo .bar {
    font-size: 1.4rem;
    }
    }

    ***

    main { + artical {...}; > p {...};
    ~ main {...};
    }

    ***

    main { & + artical {...}; & > p {...};
    & ~ main {...};
    }

-   209. Nesting in Practice


        blockquote.featured {
            order: -1;
            flex: 1 0 auto;
            background-color: black;
            color: white;
            margin-inline-start: 1rem;
            font-weight: bold;
        }
        ------
        blockquote {
            &.featured {     ----------- use '&' because 'blockquote.featured'=blockquote{&.featured}
            order: -1;
            flex: 1 0 auto;
            background-color: black;
            color: white;
            margin-inline-start: 1rem;
            font-weight: bold;
        }
        }

-   210. & and Pseudo-classes
         footer {
         text-align: center;
         }

         footer a,
         footer a:visited,
         footer a:hover {
         color: white;
         }

         ***

         footer {
         text-align: center;
         a {
         &,
         &:visited,
         &:hover {
         color: white;
         }
         }
         }

-   211.    at-rules and Nesting

            @media screen and (min-width: 768px) {
            main {
            grid-template-columns: 50px 1fr 50px;
            }
            }
            @media screen and (min-width: 1200px) {
            main {
            grid-template-columns: 1fr 900px 1fr;
            }
            }

            ***

            main {
            @media screen {
            @media (min-width: 768px) {
            grid-template-columns: 50px 1fr 50px;
            }

                    @media (min-width: 1200px) {
                        grid-template-columns: 1fr 900px 1fr;
                    }
                }

            }
            ////
            @media print {
            #aboutme {
            display: none;
            }
            }

            ***

            #aboutme {
            @media print {
            background-color: white;
            color: black;
            }
            }

# Section 25: Layers

-   213. Cascade Layers (@layer)

    -   cascade layers provide a structured way to orginize a nd balane concerns within a single origin

    audio {} - higher priority
    @layer reset{ audio[control] {}}

-   214. Defining Layers


        -   cascade layers are sorted by the order in which they first are declared, nested layers grouped within their parent layer.

        -   Can be declared:
            1. By @import rule with the layer keyword layer() function, assigning the contents of the imported file into that layer.
               @import url(resume.css)
               @import url(resume.css) layer(resume);
            2. By @layer block at-rule, assigning its child style rules into that layer.
               @import url(resume.css) layer(resume);
               @layer tonyresume {
               body {
               font-size: 40px;
               }
               }
               @layer customstyles {
               @layer tonyresume {
               body {
               font-size: 24px; ---- higest priority
               }
               }
               }
               //@layer resume, tonyresume, customstyles.tonyresume; - the same priority
            3. By a @layer statement ar-rule, declaring a named layer without assigning any rules.
                @layer resume, customstyles.tonyresume, tonyresume;
                @import url(resume.css) layer(resume);
                @layer tonyresume {
                body {
                font-size: 40px; -- highest priority beacuse of first line
                }
                }
                @layer customstyles {
                @layer tonyresume {
                body {
                font-size: 24px;
                }
                }
                }

-   215. Layers and the Cascade

    -   Cascade layers (like declarations) are sorted by order of appearance.

    -   When comparing declarations that belong to different layers, then for normal rules the declaration whose cascade layer is latest in the layer order wins, and for important rules the declaration whose cascade layer is earliest wins
        @layer resume, customstyles.tonyresume, tonyresume; -- tonyresume wins

-   216. Layers in Practice


        -   override by lightblue color
         @layer resume, customstyles.tonyresume;
         @import url(resume.css) layer(resume);
         section { ---- highest priority
         padding: 1.5rem;
         }
         @layer customstyles {
         @layer tonyresume {
         :root {
         --accent-color: lightblue;
         }
         }
         }

# Section 26: Container Queries and Units

-   217. Container Queries and Units (@container)

-   218. The Containment Module

-   219. Containment Contexts and Queries


        container-type: inline-size;
        ...
        @container (width >= 768px) {
            grid-template: repeat(2, 1fr) / repeat(5, 1fr);
            grid-template-areas:
                "portfolio anchor img1 img2 img3"
                "portfolio anchor img4 img5 img6";
        }
        ------
        container: portfoliomain inline-size; - the same as previous but with name of container
        ...
        @container portfoliomain (width >= 768px) {
            grid-template: repeat(2, 1fr) / repeat(5, 1fr);
            grid-template-areas:
                "portfolio anchor img1 img2 img3"
                "portfolio anchor img4 img5 img6";
        }

        - this approach does not let change size of pictures during changing the browser window.

-   220. Container Query Units
         #portfolio-pics {
         ....
         width: 90cqi; --- %

# Section 27: The superpower of :has

-   223. The Relational Pseudo-class

    -   Pseudo-class (for :has) - selection based on the state of the element, including the state if its children.
    -   ul:has(li.list) {...} - gives us possibility to select parent element by its children
    -   ul:has(> p.list) {...} - immediate child

-   224. :has in Practice


        -   make bold <label> element if its sibbling elemens in focus:
            .label-standard {
            ....
            &:has(~ input:focus, ~ select:focus, ~ textarea:focus) {
            font-weight: bold;
            }
            }

        - change the whole form if some element in focus inside:
        form:has(input:focus, select:focus, textarea:focus) {
        border-inline-start: solid 2px #ccc;
        padding-inline-start: 1rem;
        }

        - Make bold text in sibbling element to form
        #contactme h2 {
            &:has(~ form input:focus, ~ form select:focus, ~ form textarea:focus) {
                font-weight: bold;
            }
        }

-   225. :has in Practice (Part 2)
-   226. Native Over Custom
    -   (Browser) Native.
        Features built into browser, rather than manually created using JavaScript.
        Native features will always be faster, and more future-proof. Just be sure they're ready and supported.
        Try first make something by HTML and CSS rather than using JavaScript.

# Section 28: Modern Real-World Project: Landing Page

-   227. Landing Page
-   228. Analyzing the Designer's Prototype
-   229. Page Structure: HTML Authoring
-   230. Navigation: HTML Authoring
-   231. Hero: HTML Authoring
-   232. Features: HTML Authoring
-   233. About Us: HTML Authoring
-   234. Contact Us: HTML Authoring
-   235. Footer: HTML Authoring
-   236. Layout: CSS Authoring
-   237. Navigation: CSS Authoring
-   238. Hero: CSS Authoring
-   239.    Features: CSS Authoring: -- uses container to make items adaptive to the screen
            .features {
            padding: 3rem 1rem;
            background-color: var(--light-bg);
            text-align: center;
            width: 100%;
            container-type: inline-size;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
            h2 {
            font-size: 2rem;
            margin-bottom: 2rem;
            flex-basis: 100%; ----- make separate row of header in section
            }
            svg {
            fill: var(--primary-color);
            }
            .feature {
            @container (width >=600) {
            flex: 1;
            max-width: 300px;

                            svg {
                                margin-bottom: 1rem;
                                width: 48px;
                                height: 48px;
                            }
                        }
                        margin-bottom: 1.5rem;
                        h3 {
                            font-size: 1.5rem;
                            margin-bottom: 0.5rem;
                        }
                    }
                }

-   240. About Us: CSS Authoring
-   241. Contact Us: CSS Authoring
-   242. Footer: CSS Authoring
         footer {
         padding: 1rem;
         margin-top: auto; ---- to avoid increasing footer height if the re is no enaugh content below
         background: var(--dark-bg);
         color: var(--light-text);
         text-align: center;
         width: 100%;
         }

# Section 29: Modern Real World Project: Dashboard

-   244. Analyzing the Designer's Prototype
-   245. Page Structure: HTML Authoring
-   246. Navigation: HTML Authoring
-   247. Metrics: HTML Authoring
-   248. Table: HTML Authoring
