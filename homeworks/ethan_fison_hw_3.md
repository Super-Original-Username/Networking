# HW 3

## Ethan Fison

1. TCP RDS is required to ensure that packets are received in the the correct order. Link reliability alone does not guarantee this.
2. In the case of image transfer, any packet loss would be intolerable. This means that TCP would be the preferred protocol, as any lost packets can be resent.
3. Sequence numbers are used to determine if data has been retransmitted. Timers are used to determine if data has been lost, i.e. if an ACK has not been received within a set period of time, the packet is then marked for retransmission
4.  `01010011 + 01100110:`
    ```
      01010011

     +01100110
     __________

      10111001
    ```
    `10111001 + 01110111:`
    ```
      10111001 

    + 01110111
     __________

      00101110
    
    ```
    The one's complement of `00101110` is:
    > 11010001
    UDP takes the one's compliment of the sum as an error detecting measure. If there are any 0s in the sum, then there was an error in the segment. All 1-bit errors will be detected, as they will result in a bit within the sum flipping.

5. The image strats with the `Slow start phase`, in which the amount of packets sent exponentially increases until the threshold is hit. The image then enters the `Congestion avoidance phase`, in which the window size increases in a linear fashion. The image also contains the `Congestion detection phase`, in which the window size is decreased, and transmission is returned to either the avoidance phase or the slow start phase.