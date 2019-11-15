# CSCI 466 Homework 4

## Ethan Fison

### 1. What is the difference between routing and forwarding?

Routing is a process that occurs over an entire network, and is what determines the end-to-end paths that packets should take between sender/receiver. This is a relatively slow process, and is typically implemented via software.

Forwarding is a hardware-level function of routers that is used to transfer packets from input and output interfaces. This is a relatively very fast process, compared to routing.

### 2. Describe how packet loss can occur and be eliminated at:

#### A. Router input ports?

If packets arrive faster than the current fabric switching rate allows, then they must start queueing at the input interfaces. If the queue can't clear quickly enough,any overflow will result in packet loss. This can be prevented by having a fabric switching rate of n (the number of input ports) times the input line speed.

#### B. Router output ports?

Packet loss can occur if any ouput port receives packets at a rate fater than the line speed. This can cause a similar overflow and resultant packet loss to the situation described in (A).

### 3. Translate the given forwarding rules into a forwarding table that uses longest prefix matching to forward packets to the correct interface. Your table should list prefix match and forwarding interface.

|Prefix|Interface|
|:-----|-----:|
|11100000  00|0|
|11100000  01000000|1|
|11100000|2|
|11100001  1|3|
|Otherwise|3|



### 4.

#### A.  How a hierarchical organization of the Internet allows it to scale to millions of users?

A hierarchical system allows for extensibility of all layers without having impacts on otehr layers.

#### B. Why are there different inter- and intra-AS routing systems on the internet

