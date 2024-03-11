OBJECTIVES
The objective of the project is to build, simulate and configure different types of queuing like best effort, 
priority queue, round robin queue, weighted round robin queue and token-bucket queue. These queuing 
mechanisms are to be simulated to campare between all queuing types from different Quality of service 
(QOS) prespective. Traffic has to be classified, marked, and treated based on its characteristics such as time 
sensitive traffic voice and video and non-time sensitive traffic FTP, HTTP etc.

![1](https://github.com/ammaramin763/My-works/assets/162980561/b9cd229c-27e9-49de-a7e7-bd7598288d15)


INTRODUCTION
This is Phase 3 of project in which Project 1: Multiple Quality of Service Queuing has been implemented 
and simulated in Omnet++ Simulator . In this project , we are deploying different types of queuing like best 
effort, priority queue, round robin queue and weighted round robin queue. The router traffic is being treated 
based on its characteristics such as time sensitive traffic voice and video and non-time sensitive traffic FTP, 
HTTP etc. The concept and theory behind the implementation are as follows :
Priority Queuing(PQ)
In Priority Queuing, instead of using a single queue, the router 
bifurcates the memory into multiple queues, based on some 
measure of priority. After this, each queue is handled in a FIFO 
manner while cycling through the queues one by one. The 
queues are marked as High, Medium, or Low based on priority. 
Packets from the High queue are always processed before 
packets from the Medium queue. Likewise, packets from the 
Medium queue are always processed before packets in the 
Normal queue, etc. As long as some packets exist in the High 
priority queue, no other queue’s packets are processed. Thus, 
high priority packets cut to the front of the line and get serviced first. Once a higher priority queue is 
emptied, only then is a lower priority queue serviced.
First-In, First-Out Queuing (FIFO)
The default queuing scheme followed by most routers is FIFO. This generally requires little no configuration 
to be done on the server. All packets in FIFO are serviced in the same order as they arrive in the router. On 
reaching saturation within the memory, new packets attempting to enter the router are dropped (tail drop). 
Such a scheme, however, is not apt for real-time applications, especially during congestion. A real-time 
application such as VoIP, which continually sends packets, may be starved during times of congestion and 
have all its packets dropped.
Round Robin Queuing (RR)
RR is a queuing discipline that is quite a contrast to priority queuing. In simple RR, we have a few queues, 
and we assign traffic to them. The RR scheduler processes one packet from one queue and then a packet 
from the next queue and so on. Then it starts from the first queue and repeats the process. No queue has 
priority over the others, and if the packet sizes from all queues are (roughly) the same, effectively the 
 Figure 1 Priority Queuing model
interface bandwidth is shared equally among the RR queues. With RR, no queue is in real danger of 
starvation, but the limitation of RR is that it has no mechanism available for traffic prioritization.
Weighted Round Robin Queuing (WRR)
A modified version of RR, Weighted Round Robin (WRR), allows us to assign a "weight" to each queue, 
and based on that weight, each queue effectively receives a porti
