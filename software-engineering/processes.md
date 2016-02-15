# Processes
Related Slides: [WE07processes-requirements](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Slides/WE07processes-requirements.pdf)

Web Application development is usually a process that is executed by many persons cooperatively. Thus the process has to be organized and controlled. The process should (at least) be defined to such an extent that it is manageable and repeatable (CMM-2). Development (and maintenance) processes have

* **A logical structure** which defines the activities to be done
* **An organizational structure** which defines the coordination of the cooperative work

## Logical Structure
There are 3 *dimensions* to development activities in web applications:

* The **levels** (concerns) to be described
* The **aspects** (viewpoints) they subsume
* The **phases** (abstraction levels) they belong to

Ignore the terms above and you basically get a list of stuff that needs to be done to develop a web application.

### Levels

* **Content** The information and application logic underneath
* **Hypertext** The structuring of the content into nodes and links
* **Presentation** The user interface and page layout

The levels have to be mapped to each other.

### Aspects

* **Structural Descriptions** describe relations between objects (using class- object and package-diagrams)
* **Behavioural Descriptions** describe control- and dataflows and state-transitions (using activity-diagrams and state-charts)

### Phases

* **Requirement Engineering**
* **Design** Modeling and architecture engineering
* **Implementation and Testing**

Along these phases the descriptions become more and more concrete (less abstract).


## Organizational Structure
It is not sufficient to do pure Code-And-Fix, i.e. immediately starting to program, removing bugs that occur during testing, improving the code and add new functionality ad libitum. This leads to problems for real-life applications, since the overview on the system gets lost.

Thus, engineering is necessary. Engineering implies

* Definition of requirements
* Building of abstract models
* Implementation along these descriptions
* Quality assurance

To handle the development of the three dimensions, effective processes have to be defined, to:

* Help the team understand what it has to do
* Coordinate the work of the different developers
* Support the manager to control the actions

### Process Models

*Related exercise:* [Exercise 4.1.b](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise4-Deadline16Dec2015/Exercise4.pdf)

Process Models describe the relevant tasks for software development and their organisation. A good process model helps to

* Make experience transferrable
* Reduce risks, since the process becomes plannable

But wee need good balance between standardization and room for creativity.

Examples for Process Models are:

* Waterfall models
* V-models (e.g., V-model XT)
* Incremental models (e.g., Rational Unified Model)
* Agile models

Nice article that describes and compares Waterfall- and Agile Models: [Waterfall vs. Agile: Which is the Right Development Methodology for Your Project?](http://www.seguetech.com/blog/2013/07/05/waterfall-vs-agile-right-development-methodology)
