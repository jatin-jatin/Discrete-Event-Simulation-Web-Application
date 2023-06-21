# Discrete-Event-Simulation-Web-Application

## Project Description
This project simulates the following charateristics of a Web application with requests in a closed loop:

* Multi-Core Server Machine
* Multi-threaded Web Server
![Web-server-system-diagram](https://github.com/jatin-jatin/Discrete-Event-Simulation-Web-Application/blob/main/pictures/Web-Server-System-new.png)
* Thread-per task model - with buffering for requests
* Round-robin scheduling
* Request time-outs with retries
* Users in closed loop with think time
* Execution Time and timeout - options for distribution

<!-- **Web server system with request in a closed loop** -->
## Discrete Event Simulation
### Features of a Discrete Event Simulator
* There are events which happen discretely. 
* All events are processed from a queue called the event queue. 
![Discrete-Event-Simulation-Diagram](https://github.com/jatin-jatin/Discrete-Event-Simulation-Web-Application/blob/main/pictures/Discrete-Event-Simulator-General.png)
* The current event is the event which is popped from the queue.
* Based upon the event corresponding event handler is called.
* The event handler itself leads the creation of more events.
* This cycle continues till a specified condition or the queue becomes empty.

In our Simulation there are 4 events with 4 corresponding event handlers:
1. Request Arrival - onArrival()
1. Thread Context Switch - onContextSwitch()
1. Thread Preemption - onPreemption()
1. Request Departure - onDeparture()

*For more details check the **[simulation.cpp](https://github.com/jatin-jatin/Discrete-Event-Simulation-Web-Application/blob/main/src/simulation.cpp)** file*
## Build Instructions
### Linux
**Build Instructions**
```
$ mkdir build  
$ cd build  
$ cmake ..  
$ make
```
**To run** (make sure you are in **./build/src** from the root directory of this project)
```
$ ./main
```
## Performance Metrics
### Average Response Time vs number of users
![Discrete-Event-Simulation-Diagram](https://github.com/jatin-jatin/Discrete-Event-Simulation-Web-Application/blob/main/pictures/resptime-vs-users.png)
### Throughput vs number of users
![Discrete-Event-Simulation-Diagram](https://github.com/jatin-jatin/Discrete-Event-Simulation-Web-Application/blob/main/pictures/tput-vs-users.png)
### Average core utilization vs number of users
![Discrete-Event-Simulation-Diagram](https://github.com/jatin-jatin/Discrete-Event-Simulation-Web-Application/blob/main/pictures/util-vs-users.png)