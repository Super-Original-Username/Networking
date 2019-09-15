# Homework 1

Ethan Fison

### Question 1.

Standards are important because they provide a basic model to follow, enabling interoperability and consistency between systems.

### Question 2.

The layers are:
- Application
  - This is what end users most often deal with, such as browsers, social networking programs, etc.
- Transport
  - This controls the data transfer between points - destination, data rate, etc
- Network
  - This primarily controls paths between networked devices
- Data link
  - This handes direct conections, i.e. node-node
- Physical
  - This covers the electronics: cables, antennas, etc.

### Question 3.

With data transmission at a steady rate over a long period of time, packet-switched would be ideal. This would leave the network open for other traffic, and as long as the transmission rate is able to stay within the available time slot given by the network switch, packet loss would be minimal.

### Question 4.

Given values:
- R (transfer rate)= 2Mbps
- L (packet size)= 56Bps = 448bps
- d<sub>prop</sub> = 10ms
- Bitrate = 64Kbps
- N = 1

*From the text:*

<center>

d<sub>end-end</sub> = N(d<sub>proc</sub> + d<sub>trans</sub> + d<sub>prop</sub>)

</center>

*Using the fomulas for delay, we get:*

<center>

d<sub>proc</sub> = L÷Bitrate = 448bps÷64kbps = 7ms

d<sub>trans</sub> = L÷R = 448bps÷2Mbps = .224ms

⟹ d<sub>end-end</sub> = (1)(7ms + .224ms + 10ms) = 17.224ms

</center>

### Question 5.

a) Using one path at a time, the max rate will be determined by *min(rᵏ₁,rᵏ₂, ...,rᵏ<sub>N</sub>)*

b) For a parallel connection, this will be K ∙ min(rᵏ₁,rᵏ₂, ...,rᵏ<sub>N</sub>), the sum of the minimum capacity of each path.

### Question 6.

a) The probablity that a packet will be lost along *L* links with loss probablity *p* is 

<center>

*1 - (1 - p)ᴸ*

</center>

as subtracting the likelihood that a packet will arrive from 1 gives us the likelihood that it will not arrive.

b) Sending 4 packets will give a likelihood of

<center>

*4(1 - (1 - p)ᴸ)*

</center>

it is now 4 times less likely for all packets sent to arrive perfectly.