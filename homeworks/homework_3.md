# HW 3

## Zan Rost-Montieth

Read Chapter 3 in your textbook and the relevant lecture slides. Answer the questions below individually. The goal is to have you think about the problems, not cover every eventuality. Shoot for short, succinct answers that address the root of the question. Please, submit your typed answers as pdf/txt into the Dropbox on D2L into the “HW 3” folder.

1. [2 points] If all the links in the Internet were reliable, would the TCP reliable delivery service be redundant? Why or why not?
   - If we didn't have to worry about packet loss we would still need to implement tcp in order to ensure packets can be properly ordered on arrival.
2. [2 points] If you are to develop an application that sends high quality images from one end to another, would you prefer TCP or UDP? Explain, why you have selected that protocol (TCP/UDP)? Put some strong arguments.
   - TCP, because we are sending large files and packet loss would ruin our images
3. [2 points] In the rdt protocols described in class (and covered in textbook Section 3.4) what is the purpose of sequence numbers and of timers.
    We use timers to ensure that packets are in fact lost and not just takig a longer path through the internet. We need sequence numbers so we can replace lost packets and order packets on arrival
4. [4 points] UDP and TCP use 1s complement for their checksum. Suppose you have the following three 8-bit bytes: 01010011, 01100110, 01110111. What is the 1s complement of the sum of these 8-bit bytes? Why is it that UDP takes the 1s complement of the sum: that is, why not just use the sum? With the 1s complement scheme, how does the receiver detect errors? Is it possible that a 1-bit error will go undetected?

    ```
      01010011
    + 01100110
    ------------
      10111001
    + 01110111
  
    -----------
      00110000 with wrap
    = 00110001
    ```

   - we have to take the 1s compliment, otherwise errors could be disquised as an ignored overflow. if we didn't take 1's compliment we would need additional space to transmit the overflow which would increase transfer size. The reciever will detect error by reading a 0 in the final sum. With this method All one bit errors will be detected but a two bit error may slip through.

5. [5 points] List all possible Congestion Control mechanism considering the following image and explain all of them in detail.
    - Slow Start Phase
      - shown by the exponential curve at the beginning 
      - This is TCP connection ensuring a good connection before sneding many packets
    - Congestion Avoidance Phase
      - can be observed by the shallow slope of the first linear section
      - this is to avoid slowing the network speed
    - Congestion Detection Phase
      - this is evident by the drop after the first veritcal line
      - this drop ensures you are not taking too much bandwith
  
![chart from the hw](\homework_3.png)
