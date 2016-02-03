## Internet & WWW

### The Internet
The Internet is the global system of interconnected computer networks that use the Internet protocol suite (TCP/IP) to link billions of devices worldwide. It is a network of networks that consists of millions of private, public, academic, business, and government networks of local to global scope, linked by a broad array of electronic, wireless, and optical networking technologies. The Internet carries an extensive range of information resources and services, such as the inter-linked hypertext documents and applications of the World Wide Web (WWW), electronic mail, telephony, and peer-to-peer networks for file sharing.

The lecture uses the term *node* to describe members of the Internet. Their definition is not clear, but they seem to limit the term to physical(?) computers.

See [Wikipedia](https://en.wikipedia.org/wiki/Internet).

### World Wide Web
The World Wide Web (WWW) is an open source information space where documents and other web resources are identified by URLs, interlinked by hypertext links, and can be accessed via the Internet. It has become known simply as the Web. The World Wide Web was central to the development of the Information Age and is the primary tool billions of people use to interact on the Internet.

See [Wikipedia](https://en.wikipedia.org/wiki/World_Wide_Web)

### Host
A network host is a computer or other device connected to a computer network. [Wikipedia](https://en.wikipedia.org/wiki/Host_(network))

### Server
Provides a service

### Client
Requests and uses the service

### IP Address
Every node in the Internet has a unique address (called IP address). Formats for this address are IPv4 (32 bits) and IPv6 (128 bits). They are assigned by the IANA (Internet Assigned Numbers Authority).

### Domain Names
Node addresses may also be noted as domain names, consisting of a top level domain (e.g. *de*), a subdomain (e.g. *uni-koblenz*) and a third level domain (e.g. *informatik*). A hostname is a domain name assigned to a host.

### Domain Name System (DNS)
Maps domain names to IP Addresses

### Ports
Applications on a server can be distinguished by their port number.

### Internet Protocol (IP)
The Internet Protocol (IP) supports the exchange of data between nodes.

### User Datagram Protocol (UDP)
The User Datagram Protocol (UDP) supports the unilateral transport of data packages between nodes.

### Transfer Control Protocol (TCP)
The Transmission Control Protocol (TCP) supports the establishment of connections between nodes.

### Socket
Represents a TCP-Connection.

### Byte Stream
Can be written to or read from a socket (in this context).

### Server Socket
Waits for clients and uses an idividual thread for each client.
