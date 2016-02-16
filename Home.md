This is a Wiki for Web Engineering. Lecture slides may be summerized on this page or linked pages. Summaries are mostly copy-paste with corrections or additions. Other sources may be used to help with stuff which the slides fail to explain. Composite lecture slides may be broken down into logical topics and the slide's topic-hierarchy may be rearranged. Additional material (for "independent reading") at the end of the slides is omitted for now.

# Introduction
See [[Introduction|introduction]]


# Technologies used for Web Applications

* [[Internet & WWW|technologies/internet-and-www]]
* [[Documents|technologies/documents]]
* [[Communication|technologies/communication]]
* [[Client-side technologies|technologies/client-side]]
* [[Server-side technologies|technologies/server-side]]


# Software Engineering Techniques targeted to Web Applications

*Related exercise:* [Exercise 4.1.a](https://svn.uni-koblenz.de/ist/webeng-wise1516/trunk/Exercise/Exercise4-Deadline16Dec2015/Exercise4.pdf)

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
* [[Web Application Architecture|software-engineering/architecture]]
* [[Web Services Introduction|web-services/introduction]]
* [[web-services/orchestration-bpmn]]
* [[web-services/orchestration-bpel]]
* [[Web Application Testing|software-engineering/testing]]


# Security of Web Applications

* [[Web Application Security|security/security]]


# Excercises
Install the `github-markdown`-gem if gollum does not properly render the table below.

| Excercise | Articles                              |
| --------- | ------------------------------------- |
| 1.1.a     | [[introduction]]                      |
| 1.1.b     | [[technologies/client-side]], [[technologies/server-side]] |
| 1.2       | [[introduction]]                      |
| 2.1       | [[introduction]]                      |
| 2.2       | [[technologies/documents]]            |
| 2.3       | [[technologies/documents]]            |
| 2.4       | [[introduction]]                      |
| 3.1       | [[technologies/communication]]        |
| 3.2       | [[technologies/client-side]]          |
| 3.3       | [[technologies/documents]]            |
| 3.4       | [[technologies/client-side]]          |
| 3.5       | [[technologies/client-side]]          |
| 4.1.a     | [[Home]]                              |
| 4.1.b     | [[software-engineering/processes]]    |
| 4.2       | -                                     |
| 4.3       | [[software-engineering/requirements]] |
| 5.1       | [[software-engineering/architecture]] |
| 5.2       | [[software-engineering/architecture]] |
| 5.3       | [[software-engineering/architecture]] |
| 6.1       | [[web-services/orchestration-bpmn]]   |
| 6.2       | [[web-services/orchestration-bpmn]]   |
| 6.3       | [[web-services/orchestration-bpmn]]   |
| L1.1      | ?                                     |
| L1.2      | ?                                     |
| L2        | -                                     |
| L3        | [[software-engineering/architecture]] |
| L4        | [[web-services/orchestration-bpmn]]   |



# Exam Topic Guesses

| Topic                                          | Probability | Correct? |
| ---------------------------------------------- | ----------- | -------- |
| Draw a BPMN diagram                            | high        | yes      |
| Draw a class diagram                           | medium      | yes      |
| Draw an activity diagram                       | low         | no       |
| Draw a state chart                             | low         | no       |
| Draw a use case diagram                        | low         | no       |
| Model something in XML                         | medium      | kinda    |
| Categories of Web Applications                 | high        | yes      |
| Model-View-Controller                          | medium      | yes      |
| Web Application Requirements / Quality Aspects | low         | yes      |
| Define Web Engineering                         | low         | no       |
| Challenges in Web Engineering                  | low         | no       |
| Requirement Categories                         | low         | no       |
| Web Application Architecture                   | medium      | kinda    |
| Internet vs. WWW                               | low         | no       |
| Name and explain one attack strategy           | medium      | no       |
| Something something UWE                        | high        | yes      |
| Development dimensions                         | medium      | no       |
| Thin vs. fat clients                           | low         | yes      |
| Some model driven development bullshit         | medium      | no       |
| Name the most important models for WE          | medium      | UWE      |
| Kruchten View Model                            | low         | no       |
| BPMN's relationship to BPEL                    | medium      | no       |
| Additional testing techniques for WAs          | low         | yes      |
| What is AJAX?                                  | medium      | yes      |
| Low coupling and high cohesion                 | medium      | no       |  
| CSS                                            | high        | no       |
| Servlets/JSP                                   | low         | no       |
| Aspects of security                            | medium      | yes      |

* **Topic** (for lack of a better term): Description of the topic/task/question/exercise that might by asked in the exam
* **Propability**: Estimate of how likely the topic will be asked in the exam. An entry in the table already implies a certain propability, so this is only for ranking the listed topics among themself.
* **Correct?**: To be added after the exam. Did the exam actually ask for the topic?

Topics should already include an estimate of the kind of question that could be asked.
