# Modeling for Web Applications
Related Slides: [WE08modeling](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Slides/WE08modeling.pdf)

This topic covers use application of "well-known" modeling approaches in web engineering and introduces some web application specific modeling techniques. While general modeling languages may be used fordomain-specific and functional properties of web applications, this section focuses on web specific models.


## Motivation and Background
The most important models for WE are:
* Content model (information)
* Hypertext model (navigation)
* Presentation model (look-and-feel)
* Application logic model (like for non-web applications)

Furthermore, models are a basis for model-based development and code generation. The objectives for modeling are:
* Detailed specification
  * As base for automatic model transformation
  * As input for realization / coding
* Reducing the complexity
* Documentation of design decisions
* Readable description of system structure and functionality
* Visualization of relevant system aspects

A well-defined model helps with code technological obsolence, since the models can be reused (at least in part) for future implementations.

Abstracting from the problem domain, the model can be further separated into a **Platform Independent Model** (PIM) and a **Platform Specific Model** (PSM), which is then implemented into code. The PIM can be reused to model and create implementations on multiple platforms.

The **hypertext model** is built on top of the content, and the **presentation model** is built on top of the hypertext model. There should be no redundancy in content, but there may be redundancy in the hypertext structure (i.e. allowing multiple navigation paths).


## Modeling for Web Applications

### UML Profiles and Extensions
The following options exist for defining modelling languages (an **UML extension**) within MOF:
* Definition of new meta model (not necessarily extension of UML, but could be)
* Heavy-weight extension: uncontrolled extension of UML meta model
* Light-weight extension: controlled extension of UML meta model with stereotypes, called **UML profile**

UML is a general-purpose modeling language
* UML can be adapted to become a domain-specific language (DSL)
* Domain-specific adaption of UML is called **UML Profile**
* Domain-specific extensions are indicated by stereotypes
* Notation: «stereotype»

A **UML profile** is a lightweight, domain-specific **UML extension** using stereotypes.


## Introduction to UWE
**UML-based Web Engineering** ([Homepage](http://uwe.pst.ifi.lmu.de/)) is object-oriented and UML-based. It consists of:
* An UML-based domain specific modeling language
* A model-driven methodology
* Tool support for design and code-generation

UWE uses Use Case Diagrams. **Functional Requirements** are annotated with `«processing»`, **Navigational Processes** are annotated with `«browsing»`. Each use case should be detailed by serveral **scenarios**. A scenario is a single intended run through a use case. Descriptions of scenarios may use natural language or sequence diagrams. Very similar scenarios may be described by a **scenario group**, using activity diagrams or decision tables. Scenarios help understanding the intended system and can be used for **integration tests**.

Tutorial: [UWE Requirements Model](http://uwe.pst.ifi.lmu.de/teachingTutorialRequirements.html)


## The Content
Modeling of content corresponds to conceptual modeling (domain modeling), which can be done using UML class diagrams. The content model is the first conceptual model for the database.

Further requirements may specify the behaviour of content. Usually, domain models do not have methods. But for dynamic web pages, the content-specific behavioral part (methods) of the application may be modeled, as far as it is needed on the client side. For example, possible interactions with the content on the client side may be defined using state machines.

Tutorial: [UWE Content Model](http://uwe.pst.ifi.lmu.de/teachingTutorialContent.html)


## Hypertext
Navigation modeling means specifying the possible paths through the content on top of the content model.

The **navigation structure model** (NSM) defines the structure of the hypertext. The **access model** (AM) refines the NSM with access elements.

Tutorial[UWE Navigation Model](http://uwe.pst.ifi.lmu.de/teachingTutorialNavigation.html)

### Navigation Structure Models
The navigation structure model (NSM) is a view for a given stakeholder on the content model. It is based on the concepts (classes) of the content model. They are part of UWE.

`«navigation class»` represents a visible node in the hypertext. `«navigation link»` is an allowed navigation between these nodes. UWE distinguishes **navigation links** (connect nodes in the hypertext), **process links** (point to the start node of an interaction process) and **external links** (point to external nodes).

Less important links in NSM include: **structural links** (leading to parts of a node), **perspective links** (leading to other views of the node), **contextual links** (leading to more detailed information) and **traversal links** (leading to the next sibling wrt.(?) to a parent node).

Finding a navigation model:
1. Define a navigation class for each navigation-relevant content class
2. Define navigation links for relevant associations, aggregations and compositions of the content model
3. Add multiplicities and role names from the content model
4. Add additional navigation links according to the scenarios
5. Add additional navigation links as shortcuts

### Access Models
The AM extends the navigation classes with more concrete **navigation patterns**. Navigation patterns are interaction widgets, such as  **index** (allows to select a single object out of a list), **menu** (allows the user to choose the next node), **guided tour** (walks user sequentially through multiple of nodes) **query** (allows the user to search for nodes) and special links like **home** (points to the homepage) and **landmark** (points to a page reachable from every node).

To add access structures to a navigation model:
* Mark all navigation links with multiplicity > 1 as **index**
* Mark each class with more than one outgoing navigation link as **menu**
* Use role names of outgoing navigation links as menu items


## Process Modeling
Process modeling in UWE defines the access to the workflows of the web application as well as their behavior. The required steps are:
1. Definition of process classes for processing use cases
2. Integration of process classes into the navigation model to define entry and exit points
3. Specifying the behavior of the process class using UML Activity Diagrams

*See the related slides for an example application of these steps.*


## Presentation
Presentation modeling deals with the user interface and the look-and-feel of the Web application.

A **page** is the main visualization unit in the Web.

Presentation has two goals:
* Interaction shall be simple and self-explanatory
* The user should be oriented where he/she is

The objective of presentation modeling is modeling the structure and behaviour of the user interface. It composes pages in a hierarchy of presentation elements. This results in a static presentation model and a dynamic interaction model.

Tutorial: The slides or [UWE Presentation Model](http://uwe.pst.ifi.lmu.de/teachingTutorialPresentation.html)

### Presentation Structure
`«presentation page»` describes a page presented to the user as a visualization unit. It can be composed of different presentation groups. `«presentation group»` serves to group related presentation elements, representing a logical fragment of the page, and it presents a hypertext model node. Presentation elements include:
* `«anchor»`
* `«text»`
* `«image»`

### Presentation Behaviour
Behavioral aspects can be modeled by behavior diagrams like activity diagrams. *gg.*


## Model Customization
In UWE customizations are done using `«customization»`-annotations (*see slides for an example*).


## Model Adaption
`«customization»`s allow adding conditions to navigation, content and presentation.

*The slides do not really explain this.*
