## Communication

### URI, URL, URN
A Uniform Resource Name (**URN**) unambiguously identifies a given resource (e.g., document). A Uniform Resource Locator (**URL**) unambiguously describes the access to a given resource (e.g., document) using the domain name system (DNS). A Uniform Resource Identifier (**URI**) may be a URL or a URN. See this [Stack Overflow answer](http://stackoverflow.com/a/1984225).

### MIME
The Multipurpose Internet Mail Extensions is an approach to define specific types of media.

### HTTP

*Related exercise:* [Exercise 3.1.a](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise3-Deadline2Dec2015/Exercise3.pdf)

The Hyper Text Transfer Protocol is the protocol of the World Wide Web, in the application layer, on top of the internet layer. It uses requests and responses and is stateless. Usually, the TCP connection is kept open and reused for further requests.

**XHR** (XMLHttpRequest) is an API specification for data transfer over HTTP, usually in XML format, where the response data is directly parsed into a DOM.

### Sessions

*Related exercise:* [Exercise 3.1.b](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise3-Deadline2Dec2015/Exercise3.pdf)

Since HTTP is stateless, but web applications may want to remember users to improve their service, sessions may be used. There are two ways to implement sessions (mentioned on the slides): URL Rewriting and Cookies, the latter of witch is prefered.
