# Code 401 - Read 12

## Revision

* What is the benefit of transforming data into packets?

Data is broken down into packets to increase data transfer efficiency and enable multiple pathways to one destination. The transmission of data packets travels across networks, taking the shortest path possible. So it ensures smoother and faster transmission with less latency.

[source](https://www.techevaluate.com/why-do-we-break-data-into-packets/)

* UDP is often refereed to as a connection-less protocol. Why is this?

UDP is a layer 4 transport protocol used for data transmission. It is a connection-less protocol because no connection is needed to be established between the source and destination before transmitting data.

[source](https://en.wikibooks.org/wiki/Communication_Networks/TCP_and_UDP_Protocols/UDP)

* Can a socket server application have multiple socket connections?

Yes, an established socket connection is uniquely identified by the combination of client-side and server-side IP/Port pairs. A socket server listens on a single port, and all established client connections on that server are associated with that same listening port on the server-side of the connection. Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs, and the server would be able to handle as many clients as available system resources allow it to.

* Can a socket connection application be connected to multiple socket servers?

Yes, because the ports will be different and the connection will be uniquely identified.

* Can an application be both a socket server and a socket connection?

Yes, but each should be assigned different ports.

## Terms Documentation

* **Observer Pattern**: a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.

* **Listener**: a piece of code/function that waits for an event to occur. The event listener listens out for the event happening

* **Event Handler**: a piece of code/function that will execute to respond to an event that occurred. The event handler is the code that is run in response to it happening.

* **Event Driven Programming**: a programming paradigm in which the flow of the program is determined by events.

* **Event Loop**: a programming design pattern that waits for events in a program. It works by making a request to some internal or external event providers, then calls the relevant event handlers which dispatches the event.

* **Event Queue**: responsible for sending new functions to the track for processing. It follows the queue data structure to maintain the correct sequence in which all operations should be sent for execution.

* **Call Stack**: responsible for keeping track of all the operations in line to be executed. Whenever a function is finished, it is popped from the stack.

[source](https://www.educative.io/edpresso/what-is-an-event-loop-in-javascript)

* **Emit/Raise/Trigger**: to fire/start an event.

* **Subscribe**: a js object that defines the handlers for an event.

* **database**: an organized collection of structured information, or data, typically stored in a computer system.

## Preview - Socket.io

### OSI model

It is a conceptual framework used to describe how information from a software application in one computer moves through a network to the software application in another computer. This model consists of 7 abstraction layers, and each layer performs a particular network function: [source](https://www.javatpoint.com/osi-model)

![osi model](https://www.imperva.com/learn/wp-content/uploads/sites/13/2020/02/OSI-7-layers.jpg)

### TCP and UDP

TCP isa communications standard that enables data exchange over a network. It is designed to send packets across the internet and ensure the successful delivery of data and messages over networks. TCP organizes data so that it can be transmitted between a server and a client. It guarantees the integrity of the data being communicated over a network. Before it transmits data, TCP establishes a connection between a source and its destination, which it ensures remains live until communication begins. It then breaks large amounts of data into smaller packets, while ensuring data integrity is in place throughout the process.

TCP provides reliable communication with something called Positive Acknowledgement with Re-transmission (PAR). As a result, high-level protocols that need to transmit data all use TCP Protocol.

An alternative to TCP is UDP, which is used to establish low-latency connections between applications and decrease transmissions time.

TCP includes absent or corrupted packets and protects data delivery with controls like acknowledgments, connection startup, and flow control. UDP does not provide error connection or packet sequencing nor does it signal a destination before it delivers data, which makes it less reliable but less expensive.

[source](https://www.fortinet.com/resources/cyberglossary/tcp-ip)

### Three-way handshake

It is a way of establishing TCP connections. The Protocol Data Unit of the transport layer is called a segment. Three segments are exchanged between the client and the server for a reliable TCP connection to get established. The mechanism works as following:

![three-way handshake](https://media.geeksforgeeks.org/wp-content/uploads/TCP-connection-1.png)

* **Step 1 (SYN)**: In the first step, the client wants to establish a connection with a server, so it sends a segment with SYN(Synchronize Sequence Number) which informs the server that the client is likely to start communication and with what sequence number it starts segments with.
* **Step 2 (SYN + ACK)**: Server responds to the client request with SYN-ACK signal bits set. Acknowledgement(ACK) signifies the response of the segment it received and SYN signifies with what sequence number it is likely to start the segments with.
* **Step 3 (ACK)**: In the final part client acknowledges the response of the server and they both establish a reliable connection with which they will start the actual data transfer.

Since it uses PAR, it will resend the data unit until it receives an acknowledgement. If the data unit received at the receiver’s end is damaged(It checks the data with checksum functionality of the transport layer that is used for Error Detection), the receiver discards the segment. So the sender has to resend the data unit for which positive acknowledgement is not received.

### Sockets

Sockets are commonly used for client and server interaction. Typical system configuration places the server on one machine, with the clients on other machines. The clients connect to the server, exchange information, and then disconnect.
A socket has a typical flow of events. In a connection-oriented client-to-server model, the socket on the server process waits for requests from a client. To do this, the server first establishes (binds) an address that clients can use to find the server. When the address is established, the server waits for clients to request a service. The client-to-server data exchange takes place when a client connects to the server through a socket. The server performs the client's request and sends the reply back to the client.

![sockets](https://www.ibm.com/docs/en/ssw_ibm_i_73/rzab6/rxab6500.gif)

### WebSocket

WebSocket is a computer communications protocol that provides full-duplex (bidirectional) communication channels over a single TCP connection. This protocol is located at layer 7 in the OSI model and depend on TCP at layer 4. It enables interaction between a client and a web server, facilitating real-time data transfer from and to the server through a TCP port (usually port 443 for secured connections or 80 for unsecured connections).

This is made possible by providing a standardized way for the server to send content to the client without being first requested by the client, and allowing messages to be passed back and forth while keeping the connection open. In this way, a two-way ongoing conversation can take place between the client and the server.

### Socket.IO

Socket.IO is an event-driven library that enables real-time, full-duplex (bidirectional) communication between the Client and the Web servers. It is built on top of the WebSockets API (Client side) to provide the interface and Node.js. Generally, it has two components:

1. Client-Side: the library that runs inside the browser
2. Server-Side: the library for Node.js
