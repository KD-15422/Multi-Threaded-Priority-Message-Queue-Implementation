# Multi-Threaded-Priority-Message-Queue-Implementation
Python project: Multi-threaded priority message queue system. Threads send messages with priorities, processed concurrently. Ensures thread safety, follows good design principles.

Overview:
The solution is a Python-based implementation of a multi-threaded priority message queue system. It allows threads to send messages with varying priorities, and upon receipt, the receiving thread performs a simple action concurrently using a thread pool.

Data Structures and Algorithms:

PriorityMessageQueue:

Data Structure:
Utilizes queue.PriorityQueue for efficient prioritized message handling.
Synchronization is ensured using threading.Lock and threading.Condition.

ThreadPool:

Data Structure:
Employs concurrent.futures.ThreadPoolExecutor for managing a fixed number of threads.
Thread safety is maintained with a threading.Lock.

Functions:
send_message: Allows threads to send messages with priorities, enqueues messages, and wakes up receiving threads.

process_message: Dequeues and processes messages concurrently using the thread pool.

Building and Running:

Requirements:
Python 3.x

Building:
Save the provided code in a file, e.g., message_queue_system.py.

Running:
Open a terminal in the directory containing the file.
Run: python message_queue_system.py.
Test Cases and Expected Outcomes:
Example Test Case:

Thread 0 sends priority 2 message to Thread 1.
Thread 1 sends priority 1 message to Thread 2.
Thread 2 sends priority 0 message to Thread 0.
Expected Outcome:

Threads print messages indicating sending and processing.
Actions executed concurrently via the thread pool.
Adjust test cases based on specific priorities and actions. Observe expected outcomes in printed messages.
