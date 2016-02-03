This is a Wiki for Web Engineering. I'll just summarize the slides for now and keep everything on this page until I feel the need to move some stuff for legibility. Other sources may be used to help with stuff which the slides fail to explain.

# Introduction

## Web-Applications
A Web Application (WA) is a software system based on technologies and standards of the World Wide Web Consortium (W3C) that provides Web specific resources such as content and services through a user interface, the Web browser. They must:

* be continuously available (24/7) world-wide
* have short response times
* be easy to use for heterogenous user groups
* have a pleasant look and feel
* be highly secure
* run on a large number of different platforms (e.g., browsers)
* offer up-to-date data from heterogeneous sources
* support exploratory access
* provide correctly implemented functionality

Which can be summarized by the following qualities:

* User-friendliness
* Performance
* Reliability
* Scalability
* Security

Additionally, because auf permanent changes, they require:

* Maintainability, evolvability
* Portability
* Interoperability

### Web Server
A web server is a program that delivers web pages over the Internet using the HTTP protocol.

### Web Browser
A web browser is a program that supports rendering of and interaction with web pages written in HTML.

### Protocol
A protocol is a formal description of message formats and rules for exchanging those messages.

### Types of Web-Applications
* **Document-centric** Static homepages
* **Interactive** News sites, timetables
* **Transactional** Conference registration, room booking
* **Workflow-based** E-commerce, e-government
* **Collaborative** Groupware, wiki, bscw
* **Portal-Oriented** Search engines, marketplace portals
* **Ubiquitous** Device-independent apps
* **Semantic web** last.fm
* **Social web** Weblogs, Facebook

## Web Engineering
Web Engineering (WE) is the establishment and use of sound scientific, engineering and management principles and disciplined and systematic approaches to the successful development, deployment and maintenance of high-quality Web-based systems and applications.

There are several organizations/consortia which influence Web Engineering by producing (quasi-)standards and keeping catalogues. The most important are:

* W3C
* IETF
* IANA
* ICANN



# Technologies used for Web Applications

## Internet & WWW

### The Internet
The Internet is the global system of interconnected computer networks that use the Internet protocol suite (TCP/IP) to link billions of devices worldwide. It is a network of networks that consists of millions of private, public, academic, business, and government networks of local to global scope, linked by a broad array of electronic, wireless, and optical networking technologies. The Internet carries an extensive range of information resources and services, such as the inter-linked hypertext documents and applications of the World Wide Web (WWW), electronic mail, telephony, and peer-to-peer networks for file sharing.

The lecture uses the term *node* to describe members of the Internet. Their definition is not clear, but they seem to limit the term to physical(?) computers.

See [Wikipedia](https://en.wikipedia.org/wiki/Internet).

### World Wide Web
The World Wide Web (WWW) is an open source information space where documents and other web resources are identified by URLs, interlinked by hypertext links, and can be accessed via the Internet. It has become known simply as the Web. The World Wide Web was central to the development of the Information Age and is the primary tool billions of people use to interact on the Internet.

See [Wikipedia](https://en.wikipedia.org/wiki/World_Wide_Web)

### Host
A network host is a computer or other device connected to a computer network. [Wikipedia](https://en.wikipedia.org/wiki/Host_(network))

### Server
Provides a service

### Client
Requests and uses the service

### IP Address
Every node in the Internet has a unique address (called IP address). Formats for this address are IPv4 (32 bits) and IPv6 (128 bits). They are assigned by the IANA (Internet Assigned Numbers Authority).

### Domain Names
Node addresses may also be noted as domain names, consisting of a top level domain (e.g. *de*), a subdomain (e.g. *uni-koblenz*) and a third level domain (e.g. *informatik*). A hostname is a domain name assigned to a host.

### Domain Name System (DNS)
Maps domain names to IP Addresses

### Ports
Applications on a server can be distinguished by their port number.

### Internet Protocol (IP)
The Internet Protocol (IP) supports the exchange of data between nodes.

### User Datagram Protocol (UDP)
The User Datagram Protocol (UDP) supports the unilateral transport of data packages between nodes.

### Transfer Control Protocol (TCP)
The Transmission Control Protocol (TCP) supports the establishment of connections between nodes.

### Socket
Represents a TCP-Connection.

### Byte Stream
Can be written to or read from a socket (in this context).

### Server Socket
Waits for clients and uses an idividual thread for each client.



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
A more abstract subset derivate of SGML with no pre-defined semantics. To avoid collisions of equally named tags from different sources, name spaces may be used.

#### XML Schemas
DTDs or XML Schemas may impose validity rules and thereby create XML dialects. An XML schema should define:

* The tags
* The attributes per element
* The nesting of elements
* The entities

#### XML Processors
**XML Dom** creates a tree representation of a document. **SAX** parses the document an fires events upon reaching requested points, without building a representation in memory.

### HTML
The Hypertext Markup Language (HTML) is the standard markup language in the Web. Web browsers use it to interpret and render text, images and other material into web pages.

**Pure HTML** is very similar to XML, but browsers usually try to recover from any encountered lacks in well-formedness and validity (graceful).

**XHTML** is an XML dialect, more rigorous than HTML regarding well-formedness and validity (draconian). Their advantage is, that they can be read by standard XML processors.

**HTML 5** is a new HTML specification, including the following changes:

* More semantic elements (like <section>, <article>, <header>)
* (Plug-in independent) embedding of multimedia data (by <video>, <audio>, <canvas> -elements)
* Integration of vector graphics (SVG)
* Support of mathematical formulae (MathML)
* Barrier freedom
* Handling of syntax errors (?)

### CSS
Separates rendering information from HTML markup. A **style sheet** is a list of rules, each rule consiting of a selector and a list of declarations. Multiple sheets are applyed in an cascading sequence of priority.


## Communication

### URI, URL, URN
A Uniform Resource Name (**URN**) unambiguously identifies a given resource (e.g., document). A Uniform Resource Locator (**URL**) unambiguously describes the access to a given resource (e.g., document) using the domain name system (DNS). A Uniform Resource Identifier (**URI**) may be a URL or a URN. See this [Stack Overflow answer](http://stackoverflow.com/a/1984225).

### MIME
The Multipurpose Internet Mail Extensions is an approach to define specific types of media.

### HTTP
The Hyper Text Transfer Protocol is the protocol of the World Wide Web, in the application layer, on top of the internet layer. It uses requests and responses and is stateless. Usually, the TCP connection is kept open and reused for further requests.

**XHR** (XMLHttpRequest) is an API specification for data transfer over HTTP, usually in XML format, where the response data is directly parsed into a DOM.

### Sessions
Since HTTP is stateless, but web applications may want to remember users to improve their service, sessions may be used. There are two ways to implement sessions (mentioned on the slides): URL Rewriting and Cookies, the latter of witch is prefered.

## Client-side technologies

## Server-side technologies



# Software Engineering Techniques targeted to Web Applications

## Processes & Requirements

## Modelling for Web Applications

## Web Application Architecture

## Web Services

## Web Service Orchestration: BPMN

## Web Service Orchestration: BPEL

## Web Application Testing:
