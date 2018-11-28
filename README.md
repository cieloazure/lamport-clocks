# Assignment 5
### Week 5-12/10
#### Demonstration of Lamport clock for 2 processes in GoLang

In this week's assignment we learnt about important techniques used for coordination. In distributed systems having a synchronized global clock is very difficult hence we consider relative ordering of events. The [paper](https://amturing.acm.org/p558-lamport.pdf) by Leslie Lamport is of seminal importance in Distributed systems which gives a way to have coordination in distributed systems. 

Lamport clocks provide a way to have a partial ordering of events. It introduces a concept called as "happenend before" indicated by the arrow symbol '->' relationship which enables us to achieve a partial ordering of events. 


##### Algorithm for Lamport cloks 

- Sending 
```
time = time + 1;
time_stamp = time;
send(message, time_stamp);
```

- Receiving
 ```
 (message, time_stamp) = receive();
 time = max(time_stamp, time) + 1;
 ```



