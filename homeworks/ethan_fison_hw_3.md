# HW 3

## Ethan Fison

1. TCP RDS is required to ensure that packets are received in the the correct order. Link reliability alone does not guarantee this.
2. In the case of image transfer, any packet loss would be intolerable. This means that TCP would be the preferred protocol, as any lost packets can be resent.
3. Sequence numbers are used to determine if data has been retransmitted. Timers are used to determine if data has been lost, i.e. if an ACK has not been received within a set period of time, the packet is then marked for retransmission