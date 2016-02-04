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


# W3C Web Services

A **W3C Web Service** is a closed, self-describing and modular service described by **XML-based standards**. The service components may be **distributed** and **HTTP** is used for communication. The service is **atomic** and **stateless**, transactions need to be done manually.

This stuff is an enterprisey thing used by the likes of Microsoft, IBM and SAP. That's why you never heard of it.

## SOAP

Used to mean Simple Object Access Protocol, but the acronym has been retired.

SOAP is usually used by POSTing to a HTTP endpoint, but you can potentially also use other protocols. For that reason, SOAP ignores things like HTTP status codes, except if it doesn't.

A SOAP message is an XML file that has an envelope, containing zero or more headers and a body. Note that the entire message is in the HTTP body, so you have SOAP headers in the HTTP body, but otherwise they work similar to HTTP headers in that they contain metadata about your request. Multiple headers can be used to bounce across intermediaries, which will remove “their” header from the request and forward it appropriately.

The body contains a **Remote Procedure Call (RPC)**, which is basically a method name with arguments. The service returns the result in a similar message, which contains the method result in place of the parameters.

See also [The S stands for Simple](http://harmful.cat-v.org/software/xml/soap/simple).

## WSDL

The **Web Service Description Language** is a big XML file that explains how your service works. It contains:

* type definitions (XML Schema types)
* messages (combinations of names and types)
* porttype/interface (methods you can call and which messages they accept and return)
* binding (data format (RPC, Doc/Lit etc.) and protocol (HTTP))
* service (the URL usually)

Examples:

* [Nasdaq](http://ws.nasdaqdod.com/v1/NASDAQQuotes.asmx?WSDL)
* [Bing Ads](https://adinsight.api.sandbox.bingads.microsoft.com/Api/Advertiser/AdInsight/V10/AdInsightService.svc?singleWsdl)

In practice, you generate your WSDL by letting some tool reflect on your code and your users will also generate their client code from it. And you better hope that your tools are compatible, otherwise it just doesn't work.

## UDDI

There used to be a vision where applications would dynamically find web services via **UDDI (Universal Description, Discovery and Integration)** and then pick the best one to use at runtime. You would have a directory (Broker) that you (the Provider) could register your application's WSDL to. A user (Requester) would then ask the directory to give them a suitable web application and would then communicate with them via SOAP.

This didn't pan out of course because it's a retarded idea to have several independent web applications actually be compatible enough to use them interchangably. Today, [UDDI is dead](https://en.wikipedia.org/wiki/Universal_Description_Discovery_and_Integration).


# REST

**Representational State Transfer**. This will be filled once somebody doesn't know what it is.


# SOAP vs REST

Also known as “why would you ever use SOAP over REST”. A few reasons:

* You want to use a service that's only available as SOAP.
* There's already code using SOAP and you don't want to rewrite it.
* You need stuff like transactions (WS-Transaction) or advanced security (WS-Security).
