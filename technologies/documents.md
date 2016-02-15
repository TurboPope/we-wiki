## Documents
Documents are data transferred through the HTTP, usually between Web Browser and Web Client.

### Hypertext
The term Hypertext denotes an interconnection of textual information units by links, such that the reader can immediately access the data.

Hypertext is a network of resources (called documents or pages) which are linked to each other by references (called hyperlinks or links) inside the documents.

**Hypermedia** is the extension of Hypertext to arbitrary mutimedia objects.

### Markups
A markup language is a system for annotating a document in a way that is syntactically distinguishable from the text. ([Wikipedia](https://en.wikipedia.org/wiki/Markup_language)]). Some important markups are:

* HTML
* LaTeX
* Markdown
* XML

### SGML
The Standard Generalized Markup Language is the ancestor of XML and HTML. A Document Type Definition (DTD) is a schema, imposing additional structural requirements on a SGML document.

### XML

*Related exercise:* [Exercise 2.3](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise2-Deadline17Nov2015/Exercise2.pdf)

A more abstract subset derivate of SGML with no pre-defined semantics. To avoid collisions of equally named tags from different sources, name spaces may be used.

#### XML Schemas
DTDs or XML Schemas may impose validity rules and thereby create XML dialects. An XML schema should define:

* The tags
* The attributes per element
* The nesting of elements
* The entities

#### XML Processors

*Related exercise:* [Exercise 2.2](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise2-Deadline17Nov2015/Exercise2.pdf)

**XML Dom** creates a tree representation of a document. **SAX** parses the document an fires events upon reaching requested points, without building a representation in memory.

### HTML
The Hypertext Markup Language (HTML) is the standard markup language in the Web. Web browsers use it to interpret and render text, images and other material into web pages.

**Pure HTML** is very similar to XML, but browsers usually try to recover from any encountered lacks in well-formedness and validity (graceful).

**XHTML** is an XML dialect, more rigorous than HTML regarding well-formedness and validity (draconian). Their advantage is, that they can be read by standard XML processors.

**HTML 5** is a new HTML specification, including the following changes:

* More semantic elements (like `<section>`, `<article>`, `<header>`)
* (Plug-in independent) embedding of multimedia data (by `<video>`, `<audio>`, `<canvas>` -elements)
* Integration of vector graphics (SVG)
* Support of mathematical formulae (MathML)
* Barrier freedom
* Handling of syntax errors (?)

### CSS

*Related exercise:* [Exercise 3.3](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise3-Deadline2Dec2015/Exercise3.pdf)

Separates rendering information from HTML markup. A **style sheet** is a list of rules, each rule consiting of a selector and a list of declarations. Multiple sheets are applyed in an cascading sequence of priority.
