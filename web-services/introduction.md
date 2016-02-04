**Web Services** are a controlled way of communication between applications on different web servers. They support component-based distributed solutions in a **service-oriented architecture (SOA)**.

**Services** are **specifications** of **components**. A service is 10 to 1000 times more **coarse-grained** than classes and provide **interfaces** via **small APIs**.

**Components** are the implementation of services. The relationship of services and components is N to M. A component is a piece of software that is **encapsulated**, **transparent**, **coarse-grained**, **loosely coupled** and provides an **interface** to other components.

**Service-Oriented Architecture** is an **architectural style** that defines **business functions** in form of **services** and implements **business processes** by **orchestrating** them (stringing them together). *ED: you build a model that gets transformed into a service and XML, which you can automatically execute without writing a single line of code if you live in the Jürjens world of make-believe.*

Examples:

* Advertisements:
    * Google AdSense (REST, SOAP deprecated)
    * Bing Ads or whatever Microsoft changed the name to now (SOAP)
* Stocks:
    * [Nasdaq](http://www.nasdaqdod.com/NASDAQAnalytics.asmx?v=xOperations) (REST, SOAP)
