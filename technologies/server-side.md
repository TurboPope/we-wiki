## Server-side technologies
A web server may serve static documents (files) or invoke programs that dynamically render documents.

### Apache
Apache HTTP Server is a widely used web server with a componend-based structure (modules).

### SSI
Server-Side Include (SSI) is a simple preprocessor mechanism to create an HTML page on the fly. It supports including files, program outputs (executing CGI-scripts) and values of system variables (echo) and has simple control structures.

### CGI
The Common Gateway Interface (CGI) is a convention for the cooperation between web servers and application programs. CGI delegates the generation of web content to executable
files. The CGI-script usually runs on the same host and is kept in a directory called *cgi-bin*.

### PHP
The PHP Hypertext PreProcessor (PHP) is a scripting language on the server side. Script fragments are embedded in HTML and executed by a script interpreter on the server. PHP is

* A scripting language (usually interpreted)
* Inspired by C / C++ / Java
* Object-oriented
* Has closures since 5.3 (2009)
* Supports the use of databases by function calls
* Owns an extensive API (Standard PHP Library)

### Java Servlets
Servlets are a Java-based alternative to PHP programs. Servlets are Java objects that run in a special runtime environment (servlet container) inside the web server. The servlet container

* Maps a URL to a particular servlet
* Ensures that the URL requester has the correct access rights
* Manages the lifecycle of the servlet

### Java Pages
Java Server Pages (JSP) are similar to PHP pages,in that they add server-side code to an HTML page, but they use Java as programming language. JSPs are compiled into Java servlets at runtime. It is recompiled only in case a modification occurred.
