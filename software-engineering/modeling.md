# Modeling for Web Applications
Related Slides: [WE08modeling](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Slides/WE08modeling.pdf)

This topic covers use application of "well-known" modeling approaches in web engineering and introduces some web application specific modeling techniques.


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


## UWE


## The Content


## Hypertext

### Navigation Structure Models

### Access Models


## Process Modeling


## Presentation

### Presentation Structure

### Presentation Behaviour


## Model Customization
