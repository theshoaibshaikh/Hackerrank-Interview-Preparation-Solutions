# Inserting a Node Into a Sorted Doubly Linked List

### Problem

Given a reference to the head of a doubly-linked list and an integer, **data**, create a new DoublyLinkedListNode object having data value **data** and insert it into a sorted linked list while maintaining the sort.<br>

### Function Description

Complete the sortedInsert function in the editor below. It must return a reference to the head of your modified DoublyLinkedList.
<br>
sortedInsert has two parameters:
<br>
1. head: A reference to the head of a doubly-linked list of DoublyLinkedListNode objects.
2. data: An integer denoting the value of the **data** field for the DoublyLinkedListNode you must insert into the list.

### Solution

```python

  def sortedInsert(head, data):
    node=DoublyLinkedListNode(data) 

    #check if head is null
    if head == None:
        head=node

    #check if data is less than head
    elif head.data>data:
        node.prev=None
        node.next=head
        head.prev=node
        head=node
    else:
        #locate node after which new node to be inserted
        current=head
        while(current.next != None and current.next.data <= data):
            current=current.next
        
        if current.next!=None:
            current.next.prev=node
        node.next=current.next
        node.prev=current
        current.next=node
        
    return head
```
