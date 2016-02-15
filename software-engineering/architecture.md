# Web Application Architecture


## Introduction

**Software Architecture** is the fundamental organization of a system, embodied in its components, their relationships to each other and the environment, and the principles governing its design and evolution.

### Component Diagrams

*Related exercises:* [Exercise 5.1.c](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise4-Deadline16Dec2015/Exercise4.pdf) and [Live Exercise 3](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/LiveExercises/HandoutLive3.pdf)

See [Wikipedia](https://en.wikipedia.org/wiki/Component_diagram)

Objectives of the component structure are:

* **High cohesion** within a component (elements belong together)
* **Low coupling** between components (few dependencies)
* **Reusability** of components
* **Changeability** of components (changes to one component should not affect other components)

### Viewpoints and Views
Views are instances of viewpoints. Different stakeholders may have different viewpoints.

"To illustrate the concepts of views and viewpoints, consider the example of a very simple airport system with two different stakeholders, the pilot and the air traffic controller. The pilot has one view of the system, and the air traffic controller has another. Neither view represents the whole system, because the perspective of each stakeholder constrains (and reduces) how each sees the overall system. A viewpoint is a model (or description) of the information contained in a view. In our example, one viewpoint is the description of how the pilot sees the system, and the other viewpoint is how the controller sees the system." (<http://pubs.opengroup.org/architecture/togaf8-doc/arch/chap31.html#tag_32_06>)

#### Kruchten's 4+1 architectural view model
[4+1 architectural view model on Wikipedia](https://en.wikipedia.org/wiki/4%2B1_architectural_view_model)

* **Logical View** The functionality of a system, described by use-case diagrams
* **Development View** The developer's view, described by class- or package diagrams
* **Physical View** The overall architecture, described by deployment diagrams
* **Process View** The interactions in a system, described by activity diagrams


## Architectural Styles

*Related exercises:* [Exercise 5.1](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise4-Deadline16Dec2015/Exercise4.pdf), [Exercise 5.2](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise4-Deadline16Dec2015/Exercise4.pdf), [Exercise 5.3](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise4-Deadline16Dec2015/Exercise4.pdf)

Architectural Styles are patterns of architectures.

### Layered Architectures
Layers of functionality are arranged in a stack where each layer is restricted to communication with the layer below itself.

Most software systems use three  layers:

* **Presentation layer** Encapsulates interactions with users or other systems
* **Application layer** Determines what the system actually does
* **Data layer** Deals with the organization (storage, indexing, and retrieval) of data

Occasionally, the **Application layer** is split:

* **Application layer** for concrete application logic
* **Business layer** for business logic, independent of the application using it

A **tier** is a physical component, on which (multiple) layers can be deployed. The term **Client-Server architecture** refers to an architecture with two tiers, a client and a server (duh).

**Thin clients** are tiers that encapsulate the presentation layer only, while **Fat clients** contain at least parts of the application layer.

Layering

* Reduces complexity
* Has only few constituents
* Is refineable (allows zooming)
* Supports separation of concerns

### Data Flow Architectures

*The slides on this are a mess. Apparently, this is more of a viewpoint on an architecture that describes it with transformational activities on data.*

### Data Centered Architectures
Several independent components use the services of a **common repository**. An **active repository** actively informs the components of events.

### Model View Controller Architectures
Interactive applications are often built on three different kinds of classes:

* **Model objects** contain the core functionality and the data
* **View objects** present the model to the user
* **Controller objects** manage the overall workflow

**Presentation model objects** are "sub-objects" of the real model objects, containing only the data relevant for presentation.

**Command and Query Responsibility Segregation** (CQRS) is a pattern that segregates the operations that read data (Queries) from the operations that update data (Commands) by using separate interfaces. This implies that the data models used for querying and updates are different. (<https://msdn.microsoft.com/en-us/library/dn568103.aspx>)


## Web Application Frameworks
A framework is a blueprint of a software system that supplies basic functionality in the form of an (almost) complete system, which can be adapted to a new solution by specialization of provided classes and by addition of application-specific code. A framework already contains the basic architecture.

### Zend Framework
The Zend Framework is a MVC PHP-Framework for web applications. It favors configuration over convention.


## Web Application Servers

*Related exercise:* [Exercise 5.3](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise4-Deadline16Dec2015/Exercise4.pdf)

*The slides mention some topics, loosely related to the heading, and then fail to explain them.*

A **Web server** exclusively handles HTTP requests, whereas an **application server** serves business logic to application programs through any number of protocols. ([Article on javaworld.com](http://www.javaworld.com/article/2077354/learn-java/app-server-web-server-what-s-the-difference.html))

**JavaEE** is a widely used enterprise computing platform [...]. The platform provides an API and runtime environment for developing and running enterprise software, including network and web services, and other large-scale, multi-tiered, scalable, reliable, and secure network applications. ([Article on Wikipedia](https://en.wikipedia.org/wiki/Java_Platform,_Enterprise_Edition))

An **EJB** (Enterprise JavaBean) is a server-side software component that encapsulates the business logic of an application. ([Article on Wikipedia](https://en.wikipedia.org/wiki/Enterprise_JavaBeans))

An **EJB web container** provides a runtime environment for web related software components, including computer security, Java servlet lifecycle management, transaction processing, and other web services. ([Same article on Wikipedia](https://en.wikipedia.org/wiki/Enterprise_JavaBeans))
