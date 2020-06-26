# Reverse a doubly linked list

### Problem

You’re given the pointer to the head node of a doubly linked list. Reverse the order of the nodes in the list. The head node might be NULL to indicate that the list is empty. Change the next and prev pointers of all the nodes so that the direction of the list is reversed. Return a reference to the head node of the reversed list.

### Function Description

Complete the reverse function in the editor below. It should return a reference to the head of your reversed list.<br>
reverse has the following parameter(s): <br>
* **head**: a reference to the head of a DoublyLinkedList

### Solution

```python
def reverse(head):
    current = head
    temp=None

    while(current != None):
        #swapping the prev and next pointers
        temp=current.prev
        current.prev=current.next
        current.next=temp
        current=current.prev
    if temp != None:
        head=temp.prev
    return head
```
