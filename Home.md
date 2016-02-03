This is a Wiki for Web Engineering. Lecture slides may be summerized on this page or linked pages. Summaries are mostly copy-paste with corrections or additions. Other sources may be used to help with stuff which the slides fail to explain. Composite lecture slides may be broken down into logical topics and the slide's topic-hierarchy may be rearranged. Additional material (for "independent reading") at the end of the slides is omitted for now.

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

* [[Internet & WWW|technologies/internet-and-www]]
* [[Documents|technologies/documents]]
* [[Communication|technologies/communication]]
* [[Client-side technologies|technologies/client-side]]
* [[Server-side technologies|technologies/server-side]]


# Software Engineering Techniques targeted to Web Applications
Challenges in Web Engineering include:

* **Multidisciplinarity** Multimedia experts, content authors, software architects, usability experts, database specialists and domain experts, with their own languages and jargons that have to cooperate
* **Unavailability of Stakeholders** It may be difficult to find suitable representatives that can provide realistic requirements. Some groups of stakeholders may even be unknown at RE time
* **Volatility of Requirements and Constraints** Web applications and their environments are highly dynamic (new platforms, new standards, new devices emerge)
* **Unpredictable Operational Environment** The properties of possible execution environments (bandwidth, browsers, ...) are hard to predict
* **Impact of Legacy Systems** Integration of existing software (COTS, Open Source) may be necessary for economic reasons, but possibly not compliant to the architecture
* **Significance of Quality Aspects.** Besides the standard quality properties, performance, security, availability and usability are indispensible
* **Quality of Content** Content has to be accurate, objective, credible, relevant, up-to-date, complete, and clear
* **Developer Inexperience** Many of the underlying technologies are still fairly new
* **Firm Delivery Dates** There usually are fixed schedules that have to be kept

To introduce an engineering approach into WA development classical software engineering languages, methods, and tools have to be adapted/extended to cope with these challenges and  the principles of software engineering have to be followed even more strongly.

* [[Processes|software-engineering/processes]]
* [[Requirements|software-engineering/requirements]]
* [[Modeling for Web Applications|software-engineering/modeling]]

## Web Application Architecture

## Web Services

## Web Service Orchestration: BPMN

## Web Service Orchestration: BPEL

## Web Application Testing:
