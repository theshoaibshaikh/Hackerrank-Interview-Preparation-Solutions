# Insert a node at a specific position in a linked list

You’re given the pointer to the head node of a linked list, an integer to add to the list and the position at which the integer must be inserted. Create a new node with the given integer, insert this node at the desired position and return the head node.
<br>
A position of 0 indicates head, a position of 1 indicates one node away from the head and so on. The head pointer given may be null meaning that the initial list is empty.
<br>

**Function Description** <br>
Complete the function insertNodeAtPosition in the editor below. It must return a reference to the head node of your finished list.
<br>
insertNodeAtPosition has the following parameters:
<br>
* head: a SinglyLinkedListNode pointer to the head of the list
* data: an integer value to insert as data in your new node
* position: an integer position to insert the new node, zero based indexing
<br><br>

**Solution**

```python
def insertNodeAtPosition(head, data, position):
    node= SinglyLinkedListNode(data)

    if position==0:
        node.next=head
        head=node
    else:
        i=0
        current=head
        prev= None
        while(i<position):
            prev=current
            current=current.next
            i+=1
        prev.next=node
        node.next=current
    return head
```
