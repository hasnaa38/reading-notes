# Code 401 - Read 13

## Revision

* What does it mean that web sockets are bidirectional? Why is this useful? it means that data can be transmitted between two parties in both directions, for example: from the server to the client and from the client to the server. It is useful because a device can send and receive data at the same time, so its faster, and increases the performance of the networks as it reduces collisions and dropped packets.

* Does socket.io use HTTP? Why? yes, for its initial connection setup.

* What happens when a client emits an event? if the server was configured to listen to it, it will receive that it was emitted and execute the event handler callback.

* What happens when a server emits an event? The socket that is connected to the server and configured to listen to the event will execute the event handler callback.

* What happens if a client “misses” an event? The event will be ignored. Its just like when an event occurs and there are no event listeners for that event. The socket receives the msg and doesn't find a handler for it so nothing happens with it.

* How can we mitigate this? in the client-side, define a function to handle missing events. [more](https://stackoverflow.com/questions/32816290/what-happens-with-unhandled-socket-io-events)

## Terms Documentation

* **Socket**: a software structure that serves as an endpoint for sending and receiving data across the network. Sockets are created only during the lifetime of a process of an application running in the node. A socket is externally identified to other hosts by its socket address, which is the triad of transport protocol, IP address, and port number.

* **Web Socket**: a computer communications protocol that provides full-duplex (bidirectional) communication channels over a single TCP connection. This protocol is located at layer 7 in the OSI model and depend on TCP at layer 4. It enables interaction between a client and a web server, facilitating real-time data transfer from and to the server through a TCP port

* **Socket.io**: an event-driven library that enables real-time, full-duplex (bidirectional) communication between the Client and the Web servers. It is built on top of the WebSockets API (Client side) to provide the interface and Node.js.

* **Client**: a piece of computer hardware or software that accesses a service made available by a server as part of the client–server model of computer networks.

* **Server**: a computer that provides various shared resources to clients and other servers on a network.

* **OSI Model**: a conceptual framework used to describe how information from a software application in one computer moves through a network to the software application in another computer. This model consists of 7 abstraction layers, and each layer performs a particular network function.

* **TCP Model**: a suite of protocols designed to establish a network of networks to provide a host with access to the internet. TCP/IP prepares and forwards data packets over LANs and WANs, as well as the Internet. In fact, the Internet is the world's largest TCP/IP network. TCP/IP is responsible for full-fledged internet data connectivity and transmitting the data end to end by providing other functions, including addressing, mapping and acknowledgment. TCP/IP contains four layers, which differ slightly from the OSI model. [source](https://www.techopedia.com/definition/2460/transmission-control-protocolinternet-protocol-tcpip)

![models](https://www.techopedia.com/images/uploads/2335a085-5678-472d-8bf6-509f073cce6c.png)

* **TCP**: a transportation protocol that enables data exchange over a network. It is designed to send packets across the internet and ensure successful delivery of data and messages over networks. TCP organizes data so that it can be transmitted between a server and a client. Before it transmits data, TCP establishes a connection between a source and its destination, which it ensures remains live until communication begins. It then breaks large amounts of data into smaller packets, while ensuring data integrity is in place throughout the process.

* **UDP**: a transportation protocol that enables data exchange over a network especially for time-sensitive transmissions such as video playback or DNS lookups. It speeds up communications by not formally establishing a connection before data is transferred. This allows data to be transferred very quickly, but it can also cause packets to become lost in transit.

* **Packets**: a unit of data that is transmitted from source address to a destination address over the internet or packet-switched network.

## Preview - Message Queues

### Namespaces and rooms

A **namespace** is a communication channel that allows splitting the logic of an application over a single shared connection. Each namespace has its own event handlers, rooms, and middle-wares.

To define a new namespace in the server-side, use the `of` method. To connect to it in the client-side, add it as a route to the end of the host.

[namespaces](https://socket.io/docs/v3/namespaces/)

A **room** is an arbitrary channel in a namespace that sockets can join and leave. It can be used to broadcast events to a subset of clients. To implement it in the server-side, define and listen `joinRoom` event that uses the `join(room-name)` method. In the client-side, emit that event along with the room-name you want to join to.

[rooms](https://socket.io/docs/v3/rooms/)

![rooms and namespaces](https://miro.medium.com/max/990/0*aWpdwmjqgtVCMZa6.png)

### Message Queues

A queue is a line of things waiting to be handled, starting at the beginning of the line and processing it in sequential order. A message is the data transported between the sender and the receiver application; it's essentially a byte array with some headers at the top.

A message queue is a queue of messages sent between applications. It includes a sequence of work objects that are waiting to be processed. The basic architecture of a message queue:

* producers app - creates messages and deliver them to the message queue.
* consumer app - connects to the queue and gets the messages to be processed. Messages placed onto the queue are stored until the consumer retrieves them.

![msgs queue](https://pbs.twimg.com/media/DE9ng7HXUAEg0oT.jpg)

A message queue provides an asynchronous communications protocol, which is a system that puts a message onto a message queue and does not require an immediate response to continuing processing. Messages are held until a consumer is ready to process them. And when it does so, each message is processed only once by a single consumer.

Queuing allows:

1. Communication between programs (even if they were running in different environments) without having to write the communication code.
2. Selecting the order in which a program processes messages.
3. Balancing loads on a system by arranging for more than one program to service a queue when the number of messages exceeds a threshold.
4. Increasing the availability of an applications by arranging for an alternative system to service the queues if your primary system is unavailable.

[source1](https://www.cloudamqp.com/blog/what-is-message-queuing.html), [source2](https://www.ibm.com/docs/en/ibm-mq/8.0?topic=overview-introduction-message-queuing)