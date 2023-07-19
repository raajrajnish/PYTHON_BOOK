# Python Threads

In multithreading, the concept of threads is used. Let us first understand the concept of thread in computer architecture.

# What is a Process in Python?
A thread is an entity within a process that can be scheduled for execution. For simplicity, you can assume that a thread is simply a subset of a process!
Multithreading is defined as the ability of a processor to execute multiple threads concurrently.

======================

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

1. Below is a very basic example on how to call thread in python (old way)
```
import threading
import time

# calculating the start time of the program
start = time.perf_counter()

# function which does something by taking a parameter
def do_something(seconds):
    print(f'Sleeping for {seconds} second(s)')
    time.sleep(seconds)
    print('Done sleeping')

# creating and empty list to store threads
threads = []

# running a for loop to generate threads
for _ in range(10):
    t = threading.Thread(target=do_something, args=[1.5])
    t.start()
    threads.append(t)

# calling join on generated threads - joins make sure all the threads have been executed first before moving to other
# line of code
for thread in threads:
    thread.join()

# calculating time at the end of the program
finish = time.perf_counter()

# calculating the total time take by the program
print(f'Finished in {round(finish-start,2)} second(s)')
```

2. Below is a very basic example on how to call thread in python (new way)
```
import concurrent.futures

start = time.perf_counter()

def do_something(seconds):
    print(f'Sleeping for {seconds} second(s)')
    time.sleep(seconds)
    return f'Done sleeping {seconds}'

seconds_to_wait = [5,4,3,2,1]
with concurrent.futures.ThreadPoolExecutor() as executor:
    results = executor.map(do_something, seconds_to_wait)  # return the results in the order they started
    for result in results:
        print(result)

finish = time.perf_counter()
print(f'Finished in {round(finish-start,2)} second(s)')
```




  
