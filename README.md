# Network-security

In this repository I will tell you about ping and its error messages and give you a small task

What is ping? 

in network security ping is a round trip time calculation. It is measured in Milliseconds. Ping uses ICMP (Internet Control message protocol) echo request and echo reply feature to test physical connectivity. If there will soem dropped or lost packets then the ping will display asterics (*). By default ping waits approximately 4000 ms (4 sec) for each response before displaying an error message "Request timeout".

Concept of Hops in Network Security:
Hop refers to number of routers that a packet passes through from it source to its destination. The count represents the total number of routing devices TTL (Time to live) fields. TTL value specifies approximately how many routers the packet has gone through. TTL value max can be 255 because of its size of byte 1 (8 bits -> max, value = 255). On the internet, it usually takes very less Round Trips ( RT ) to finish a request. And within each trip, with each hop TTL decreases. Most of the requests get finished without even reaching TTL value zero
You sent a request to some non-existent server/URL. At first its TTL was 255. It keeps on hopping from 1 router to other, until TTL becomes zero, which is when a packet is dropped

Why don't we need a bigger TTL value? 
If we set TTL of a packet to 10000, it keeps on hopping from one device to another (eventually TTL reaches zero and packet gets dropped) if the server/URL is not found. But think if there are lots of packets circulating, without a destination, slowing the whole network. 

Error messages:
1) Destination Host Unreachable:
This message indicates one of two problems: either the local system has no route to the desired destination, or a remote router reports that it has no route to the destination. When you ping to an IP address in a different network, ping packets reach default gateway. My default gateway sends the packet to remote gateway. So ping packet finally reaches the remote network. However, if the remote gateway failed to find the remote host, it will send an echo Destination host unreachable.
 The error message "Destination Host Unreachable” tells that the ping request from our computer cannot find the route to the destination IP address (destination host). It means, the Packet send from your computer reached the destination network successfully but the remote gateway failed to find the destination host. So the remote gateway sends an Echo message Destination host unreachable.

2) Request Timed out
By default, ping/trace route waits Approximately 4,000 milliseconds (4 seconds) for each response to be returned before displaying the "Request Timed Out" message. This error message indicates that your host did not receive the ping message back from the destination device within the designated time period. This is an indicator that the destination device is not connected to the network, is powered off, or is not configured correctly

Task:
Now your task is very simple You just have to ping my website and tell me if the packets received or loss

How to Ping?
Open command prompt and enter ping www.cyberinsights.site and enter

You can tell me the detail on my LinkedIn.
