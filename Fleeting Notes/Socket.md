
Socket is a connection between two devices using a common protcol like TCP or UDP.
In the context of internet socket is usually a combination of IP address and Port Number

1. Sending device selects a local port number to use for communication this is usually done by the OS
2. The sending device will request for the protocol to use and port number of the device to establish connection
3. The receieving device will give its own port number as respose to the request which will be used for the communication
4. Then the sending device will create a socket between two devices with the protocol and the port number from the recieving device. This socket act as endpoint for communication and data is sent upon agreed protocol
In summary, a socket is created between two devices when they want to communicate with each other using a network protocol. The process involves the two devices agreeing on a protocol, the sending device choosing a local port number, and the two devices exchanging port numbers to create a socket that identifies the specific connection between them.