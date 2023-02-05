# streaming-04-multiple-consumers
## Author: Jonathan Nkangabwa
## Date: February 4th, 2023
> Use RabbitMQ to distribute tasks to multiple workers

One process will create task messages. Multiple worker processes will share the work. 


## Before You Begin

1. Fork this starter repo into your GitHub.
1. Clone your repo down to your machine.
1. View / Command Palette - then Python: Select Interpreter
1. Select your conda environment. 

## Read

1. Read the [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)
1. Read the code and comments in this repo.

## RabbitMQ Admin 

RabbitMQ comes with an admin panel. When you run the task emitter, reply y to open it. 

(Python makes it easy to open a web page - see the code to learn how.)

## Execute the Producer

1. Run emitter_of_tasks.py (say y to monitor RabbitMQ queues)

Explore the RabbitMQ website.

## Execute a Consumer / Worker

1. Run listening_worker.py

Will it terminate on its own? How do you know? **It does not terminate on its own and will if we hit control + c to close the program**

## Ready for Work

1. Use your emitter_of_tasks to produce more task messages.

## Start Another Listening Worker 

1. Use your listening_worker.py script to launch a second worker. 

Follow the tutorial. 
Add multiple tasks (e.g. First message, Second message, etc.)
How are tasks distributed? **they are evenly distributed amongst the worker.py terminals. So with 6 tasks, and 3 worker.py files running, each will receive 2 tasks**
Monitor the windows with at least two workers. 
Which worker gets which tasks? **The terminal I opened first received its tasks. so the First in, First out method also works not only with messages in the queu, but worker.py files that are running and when they start**


## Reference

- [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)


## Screenshot

See a running example with at least 3 concurrent process windows here:

![Version1.1](v1_tasks_1_2.png)
![Version1.2](v1_tasks_3_4.png)
![Version1.3](v1_tasks_5_6.png)
![Version2.1](v1_tasks_7_8_9.png)
![Version2.2](v1_tasks_10_11_12.png)
![Version3.1](v3_tasks_14_15_16.png)