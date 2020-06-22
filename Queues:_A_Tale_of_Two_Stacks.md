# Queues: A Tale of Two Stacks

### Problem

A queue is an abstract data type that maintains the order in which elements were added to it, allowing the oldest elements to be removed from the front and new elements to be added to the rear. This is called a First-In-First-Out (FIFO) data structure because the first element added to the queue (i.e., the one that has been waiting the longest) is always the first one to be removed.
<br>
A basic queue has the following operations:
<br>
Enqueue: add a new element to the end of the queue.<br>
Dequeue: remove the element from the front of the queue and return it.<br>

In this challenge, you must first implement a queue using two stacks. Then process .q queries, where each query is one of the following 3 types:
<br>
1. 1 x: Enqueue element  into the end of the queue.
2. 2: Dequeue the element at the front of the queue.
3. 3: Print the element at the front of the queue.

### Function Description
Complete the put, pop, and peek methods. They must perform the actions as described above.

### Solution
```python
class MyQueue(object):
    def __init__(self):
        self.item=[]        
    
    def peek(self):
        if len(self.item) != 0:
            return self.item[-1]
        
    def pop(self):
        if len(self.item) != 0:
            self.item.pop()
        
    def put(self, value):
        self.item.insert(0,value)
        

queue = MyQueue()
t = int(input())
for line in range(t):
    values = map(int, input().split())
    values = list(values)
    if values[0] == 1:
        queue.put(values[1])        
    elif values[0] == 2:
        queue.pop()
    else:
        print(queue.peek())
```

