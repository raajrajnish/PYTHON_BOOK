# Python Threads

Threading in Python refers to the concurrent execution of multiple threads within a single program. A thread is a lightweight process that can perform 
tasks independently, allowing for parallelism and efficient utilization of system resources.

**Thread**: A thread represents an independent flow of execution within a program. It allows multiple tasks to run concurrently. Threads share the same memory 
space, allowing them to access and modify shared data.

When working with threading in Python, it's essential to consider the nature of your tasks. Threads are well-suited for I/O-bound operations, such as network 
requests or file operations, where the threads can overlap waiting times. However, for CPU-bound tasks that require parallelism on multiple cores, you may 
consider using multiprocessing instead.

**Advantages of Threads**
- **Concurrent Execution**: Threads allow multiple tasks to execute concurrently within a single program. This is especially useful for I/O-bound operations,
  where threads can overlap waiting times and keep the CPU busy with other tasks.
- **Resource Sharing**: Threads share the same memory space, allowing them to access and modify shared data. This can be advantageous when you need to share
  information or communicate between different parts of your program.

Python's Global Interpreter Lock (GIL) limits true parallelism by allowing only one thread to execute Python bytecode at a time. This means that threads are 
more effective for I/O-bound tasks rather than CPU-bound tasks that require parallel processing.

**CAUTION** Proper synchronization and coordination are crucial when working with threads to avoid data inconsistencies and race conditions. Depending on your requirements, 
you may want to explore other concurrency models, such as multiprocessing, asynchronous programming with **asyncio**, or external libraries like **concurrent.futures** for 
parallelism.

**Examples**
Below is a very basic example on how to call thread in python
```
"""
EXAMPLE - How to use threading in python
"""
import threading
import time

# calculating the start time of the program
start = time.perf_counter()

# function which does something
def do_something():
    print('Sleeping for 1 second')
    time.sleep(1)
    print('Done sleeping')

# creating 2 threads
t1 = threading.Thread(target=do_something)
t2 = threading.Thread(target=do_something)

# to run the threads
t1.start()
t2.start()

# make sure both threads finish first before executing next line
t1.join()
t2.join()

# calculating time at the end of the program
finish = time.perf_counter()

# calculating the total time take by the program
print(f'Finished in {round(finish-start,2)} second(s)')

Finished in 1.02 second(s)
```




  
