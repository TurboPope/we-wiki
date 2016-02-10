# Security for Web Applications
Security is a multi-faceted matter. It subsumes
* **Confidentiality** Exchanged data cannot be read by a third party
* **Integrity** Nobody is able to modify the exchanged information
* **Authentication** The identity of a requesting person or a program is verified
* **Authorization** Requesters are granted the right privileges
* **Non-repudiation** Contracts are kept by requester and provider
* **Availability** The availability of the provider is guaranteed
* **Privacy** Private data is handled reliably


## Cryptography
Encryption denotes the use of mathematical transformations of plain text into cipher text. Decryption denotes the inverse process.

Cryptography is used for
* Encryption and decryption of data (confidentiality)
* Signatures (integrity)
* Certificates (authentication)

Most cryptographic algorithms rely on **keys** as secret items.

For **Symmetric Cryptography**, receiver and sender use the same key. Examples are [Ceasar's Code](https://en.wikipedia.org/wiki/Caesar_cipher) and [DES](https://en.wikipedia.org/wiki/Data_Encryption_Standard).

Because sharing a key implies the need to communicate the key, which is risky, with **Asymmetric Cryptography** sender and receiver use a private and a public key. Messages encrypted (by the sender) with a public key (of the receiver) can only be decrypted with the private key (by the receiver). One such cryptosystem is [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem)).


## Communication Issues

### Confidentiality
The goal of confidentiality is to prevent reading of exchanged documents by a third party. This is achieved by encrypting the data which are exchanged over HTTP. **HTTPS** (HTTP secure) is offered for that purpose.

### Integrity
Integrity is the protection of the exchanged artifacts against changes by a third party. If an integrity breach cannot be avoided, it should at least be detected. To prevent modification through third parties, **digital signatures** can be used.

**Checksums** are another approach to detect forgery. A checksum is computed by a hash function that computes a small piece of data out of a possible much larger data block. **SHA-1** is a hash algorithm thart produces a small digest of a large object. Any modification leads to a completely different hash value.

### Authentication
Authentication is the verification of the identity of a person or program. For humans, a common approach for authentication is the use of passwords. For programs, **public key authentication** may be used.

A **digital certificate** binds the public key to the identity of the private-key holder and are issued by certification authorities (CAs) like Symantec (formerly VeriSign).

### Authorization
Authorization aims at identifying the privileges that authenticated users are granted. It may depend on the identity of the user or some characterizing attributes.

* **Access Control Lists** (ACL) declare access permissions for individual users or groups
* **Role-based access control** (RBAC) assigns privileges and prohibitions to roles

### Non-repudiation
Non-repudiation refers to the property that client and server cannot appeal against their own statements, e.g. customers must not be able to deny orders they placed. Non-repudiation is achieved through **authentication** and **integrity**.


## Client-side Issues
**Mobile code** (e.g. Javascript) originates from the server but is executed on the client. Malicious mobile code leads to severe risks:
* Eavesdropping
* Unauthorized access to the local file system
* Misuse of the local system for further attacks

Countermeasures include:
* **Sandboxing** Executes code in an restricted environment
* **Fine grained access control** Single actions are checked for authorization
* **Code signing** A guaranty for the integrity and trustworthiness of mobile code (end users have to decide
whether they trust or not)

**The same-origin policy** is an important concept in the web application security model. Under the policy, a web browser permits scripts contained in a first web page to access data in a second web page, but only if both web pages have the same origin. An origin is defined as a combination of URI scheme, hostname, and port number.[1] This policy prevents a malicious script on one page from obtaining access to sensitive data on another web page through that page's Document Object Model. ([Wikipedia](https://en.wikipedia.org/wiki/Same-origin_policy))


## Server-side Issues

### Cross-site scripting
Cross-site scripting (XSS) enables attackers to inject client-side scripts into web pages. A cross-site scripting vulnerability may be used by attackers to bypass access controls such as the same-origin policy. See [Wikipedia](https://en.wikipedia.org/wiki/Cross-site_scripting#Types) for concrete attack strategies.

An related attack is **SQL injection**, where inputs of the user are directly executed as SQL statements ([XKCD](https://xkcd.com/327/)).

### Privacy
Privacy demands the reliable handling of data, like personal information, for example contact data or credit-card information.

#### P3P
P3P is a protocol for websites to declare their intended use. P3P policies describe
* Which information the server stores
* Use of the collected information
* Permanence
* Visibility

Customers can declare their privacy preferences using P3P agents (e.g. Firefox, Internet Explorer) which automatically check the P3P policy before accessing a web page.
