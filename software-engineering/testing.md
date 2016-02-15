# Quality Assurance for Web Applications

Quality Assurance (QA) comprises all planned and systematically performed activities to assure an acceptable level of trust, that something meets given requirements.

Traditional quality assurance techniques concentrate largely on functional requirements using inspection and testing techniques.

Web applications additinally need to take non-functional requirements like **usability**, **reliability**, **availability**, **browser compatibility**, **efficiency**, **maintainability**, **portability** and **security** into account by measuring, inspecting and testing.


## Testing
Testing is the experimental assessment of concrete artifacts with respect to their correctness and/or their quality properties.

### Specifics of Web Applications
There are (often) special risks for WAs:

* **Lack of skill of the team** Poor acceptance of methodologies
* **Immaturity of methods** For some new technologies there are no tools yet
* **Dominance of change** Tests have to be adapted to changing requirements
* **Immature third party components** Dependence on unvalidated sources

**Test-Driven Development** (TDD) uses tests as manifestations of requirements:
1. Define automated tests
2. Produce code to pass the test
3. Refactor the code to conform to standards
4. Do regression tests

Web Applications have more testing dimensions:

* **Content** requires proofreading, spell checking, checking of domain specific constraints
* **Hypertext structure** requires checking accessibility of pages, broken links and state changes when going back in history
* **Aesthetics** Review presentation, let experts evaluate adequacy
* **Multi-platform delivery** Simulate devices
* **Multilinguality and usability** Recognize cultural interdependencies, do excessive beta testing


### Techniques for Web Applications
The goal of **functional testing** is to find **errors**. An error is the difference between a computed, observed, or measured value or condition and the true, specified, or theoretically correct value or condition.

**Usability testing** evaluates the ease-of-use of different Web designs, the overall layout, and the navigations of a Web application for different users. It is usually done in a laboratory setting, using workrooms fitted with one-way glass, cameras, etc..

**Link testing** systematically follows all links and produces a link graph (sitemap).

**Security testing** simulates attacks systematically.

**Load testing** generates requests which are sent to the Web application concurrently by simulated users.

**Browser testing** aims to discover errors because of inconsistencies between browsers.

One may also use metrics to get deeper insight on the quality of a Web application:

* Depth and breadth of the navigation structure
* Distance between two related pages
* Load time of pages
* Latency of request handling
* Size of transferred documents
