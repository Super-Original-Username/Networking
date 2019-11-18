# CSCI 440 Homework 5

## Ethan Fison

### 1. What are the differences between the following types of wireless channel impairments- “path loss”, “multipath propagation” and “interference” from other sources?

**Path Loss**: This results from decreases in signal strength due to distance and pysical interference (from walls and the like).

**Multipath Propagation**: Packet loss resulting from radio signals reflecting off of surfaces, causing some packets to take longer than anticipated to arrive.

**Interference**: Packet loss resulting from radio signals colliding and impacting signal contents.

### 2. What are the differences between a master device in a bluetooth network and base station in 802.11 network?

Bluetooth organizes itself into a piconet of up to eight devices, with one acting as the master, which determines the hopping pattern based on its clock. Slave devices within the piconet have to match that hoppign pattern. Piconets can overlap into something called a Scatternet.

802.11 uses a base station for transmission and receipt of data between all devices on the network, serving as a hub for the entire network.

### 3. If a node has a wireless connection to the Internet, does that node have to be mobile? Suppose that a user with a laptop walks around her house with her laptop, and always accesses the Internet through the same access point. Is the user mobile from a network standpoint? Explain.

Since the access point does not change while the connection is active, the user is not mobile. Mobility is defined the ability of a node to maintain a connection while changing access points over time.

### 4. What are the purposes of the HLR and VLR in GSM networks? What elements of mobile IP are similar to the HLR and VLR?

HLR is a database used to store a subscriber's number, information, and last known location. These data points are used to route information to the correct AP for the device.

VLR is used to enable services for a subscriber on another network using information from that subscriber's HLR.

Edge routers on home and foreign networks are similar to GSM's HLR and VLR, respectively.

### 5.  What feature in 3G and 4G network made them popular in terms of massive user and connected devices? What are the roles EPC in 4G architecture?

### 6. Why is a packet that is received after its scheduled playout time considered lost?