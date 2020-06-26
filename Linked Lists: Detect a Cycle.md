# Linked Lists: Detect a Cycle

### Problem

A linked list is said to contain a cycle if any node is visited more than once while traversing the list. For example, in the following graph there is a cycle formed when node **5** points back to node **3**.

### Function Description

Complete the function has_cycle in the editor below. It must return a boolean true if the graph contains a cycle, or false.<br>
has_cycle has the following parameter(s):
* **head**: a pointer to a Node object that points to the head of a linked list.

### Solution
```python
def has_cycle(head):
    current=head
    s=set()
    while(current!=None):
        if current in s: #if node already in set then cycle
            return True
        
        s.add(current) #adding node to set
        current=current.next
    return False
```
