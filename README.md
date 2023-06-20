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
In our Simulation there are 4 events with 4 corresponding event handlers:
1. Request Arrival - onArrival()
1. Thread Context Switch - onContextSwitch()
1. Thread Preemption - onPreemption()
1. Request Departure - onDeparture()

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
* Avg. Response Time vs number of users
* Throughput, Goodput, Badput vs number of users
* Request Drop rate vs number of users
* Avg. core utilization vs number of users