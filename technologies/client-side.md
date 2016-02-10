## Client-side technologies
*Related exercise:* [Exercise 1.1.b](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise1-06Nov2015/)

Since the higher stages of the Web require dynamic, interactive pages, new technologies are needed to "bring life into HTML". Helper programs are applications that add functionality to browsers (?). Plugins are permanent helper programs. Often, media files like PDFs are forwarded to such plugins. Other approaches include applets and scripting languages.

### Java Applets
*Related exercise:* [Exercise 3.5](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise3-Deadline2Dec2015/Exercise3.pdf)

Applets are small applications (written in a compiled language) for a specific task which are started from the web page and loaded and executed by the browser. The lecture discusses Java Applets as an example. [Java Applets are deprecated](https://blogs.oracle.com/java-platform-group/entry/moving_to_a_plugin_free). Java Applets are:

* Not programs (no main-method)
* Input and output are done via the applet’s GUI
* They are event-driven
* They are executed in a sandbox (but can give further permissions, cf. Chapter on security later this semester)

[Wikipedia Article](https://en.wikipedia.org/wiki/Java_applet)

### Scripting Languages
A scripting language is a programming language that controls the execution of other applications. They are (usually) interpreted whereas applications controlled by them are (usually) compiled and may be embedded in the applications
they control. In the context of web applications, client-side scripts are used to make content more "alive" (dynamic), while server-side scripts control the production of content.

### JavaScript
*Related exercise:* [Exercise 3.2](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise3-Deadline2Dec2015/Exercise3.pdf)

JavaScript is a scripting language used in browser. It is used to support (for example)

* User interaction
* Browser control
* Asynchronous communication with the server
* Document manipulation
* Form validation
* Dynamic changes of content

It is

* Weakly typed (dynamically typed) (unlike Java),
* Prototype-based (unlike object-oriented languages)
* Supporting first-class functions (like functional languages)
* Case sensitive (unlike HTML)

The lecture discusses aspects JavaScript as a programming language in detail. Refer to [Wikipedia](https://en.wikipedia.org/wiki/JavaScript) for an alternative overview of the language.

### JSON
The JavaScript Object Notation is a lightweight notation for structured data, often used as an alternative to XML. **Please do not use `eval()` to parse JSON in JavaScript, like the lecture tells you to**. Use `JSON.parse()` instead, since `eval()` executes the given code, [which is a big security risk](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval#Don't_use_eval_needlessly!).

### AJAX
*Related exercise:* [Exercise 3.4](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise3-Deadline2Dec2015/Exercise3.pdf)

AJAX (Asynchronous JavaScript and XML) is a set of web development techniques using many web technologies on the client-side to create asynchronous Web applications. With Ajax, web applications can send data to and retrieve from a server asynchronously (in the background) without interfering with the display and behavior of the existing page.

See [Wikipedia](https://en.wikipedia.org/wiki/Ajax_(programming)).
