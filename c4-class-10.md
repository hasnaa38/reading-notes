# Code 401 - Read 10 - Stacks and Queues

## Stacks

A stack is a container of objects that are inserted and removed according to the last-in first-out (LIFO) principle.
Objects are called Nodes, where each Node references the next Node in the stack, but does not reference its previous.

### Stacks common terminology

1. *Push* - for adding Nodes to a stack
2. *Pop* - for removing Nodes from a stack. Popping from an empty stack will raise an exception
3. *Top* - the top of a stack
4. *Peek* - the value of the top Node in a stack. Peeking an empty stack will raise an exception
5. *IsEmpty* - returns true when stack is empty otherwise returns false.

![stack](https://miro.medium.com/max/761/1*kJIoFVwgiVGM9Rkd71OMEw.png)

### Stacks concepts

* Push -> *FILO* - First In Last Out: the first item added in the stack will be the last item popped out of the stack.
* Pop -> *LIFO* - Last In First Out: the last item added to the stack will be the first item popped out of the stack.

![FILO&LIFO](https://vivadifferences.com/wp-content/uploads/2020/03/Stack-Data-Structure.jpg)

### Pushing

To add a new Node to a stack, push it into the stack by assigning it as the new top, with its next property equal to the original top.

1. Define the Node that you want to add
2. Assign the next property of new Node to reference the same Node that top is referencing
3. Re-assign the top so it references the new Node

This is an O(1) operation because it takes the same amount of time no matter how many Nodes there are in the stack.

### Popping

To remove a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.

1. Check isEmpty to ensure no exceptions are raised. Alternately, you can wrap the call in a try/catch block
2. Create a reference named temp that points to the same Node that top points to
3. Re-assign top to the value that the next property is referencing
4. Clear out the current temp next property
5. Return the value of the temp Node

This is an O(1) operation because it takes the same amount of time no matter how many Nodes there are in the stack.

### Peek

When conducting a peek, you will only be inspecting the top Node of the stack. Check isEmpty to ensure no exceptions are raised. Alternately, you can wrap the call in a try/catch block.
This is an O(1) operation because it takes the same amount of time no matter how many Nodes there are in the stack.

### IsEmpty O(1)

Check if the top is null. This is an O(1) operation.

## Queues

A queue is a container of objects (a linear collection) that are inserted and removed according to the first-in first-out (FIFO) principle.

### Queues common terminology

1. *Enqueue* - for adding Nodes to a queue
2. *Dequeue* - for removing Nodes from a queue. Popping from an empty queue will raise an exception
3. *Front* - the front/first Node of a queue
4. *Rear* - the rear/last Node of a queue
5. *Peek* - the value of the front Node in a queue. Peeking an empty queue will raise an exception
6. *IsEmpty* - returns true when queue is empty otherwise returns false.

![queue](https://benoitpasquier.com/images/2020/03/queue-data-structure.png)

### Queues concepts

* Push -> *FIFO* - First In First Out: the first item in the queue will be the first item out of the queue.
* Pop -> *LILO* - Last In Last Out: the last item in the queue will be the last item out of the queue.

![fifo](https://prepinsta.com/wp-content/uploads/2020/04/Queue-Data-Structures-1024x1024.png)

### Enqueue O(1)

To add an item to a queue, you use the rear next property. 

Let’s walk through the process of adding a Node to a queue:

1. Change the next property of the rear to point to the Node we are adding.
2. Re-assign the rear reference to point to the new Node 5.

This is an O(1) operation in time because it does not matter how many other items live in the queue (n); it takes the same amount of time to perform the operation.

### Dequeue

To remove an item from a queue:

1 Check isEmpty to ensure no exception are beinng raised. Alternately, you can wrap the call in a try/catch block
2. Create a temporary reference type named temp and have it point to the same Node that front is pointing to
3. Re-assign front to the next value that the Node front is referencing.
4. Re-assign the next property on the temp Node to null
5. Return the value of the temp Node that was just removed

This is an O(1) operation in time because it doesn’t matter how many other items are in the queue, you are always just removing the front Node of the queue.

### Peek
When conducting a peek, you will only be inspecting the front Node of the queue. Check isEmpty to ensure no exceptions are raised. Alternately, you can wrap the call in a try/catch block.
This is an O(1) operation because it takes the same amount of time no matter how many Nodes there are in the stack.

### isEmpty

This is an O(1) operation because it takes the same amount of time no matter how many Nodes there are in the stack.

## Stack vs Queue

![stack vs queue](https://4cawmi2va33i3w6dek1d7y1m-wpengine.netdna-ssl.com/wp-content/uploads/2018/07/Computer-science-fundamentals_6.1.png)

| stacks | Queues |
|--------|--------|
| Based on the LIFO principle | Based on the FIFO principle|
| Pushing and popping takes place only from one end of the list | Enqueuing and Denqueuing takes place from the opposite ends of the list |
| Only one pointer is maintained to access the list (top) | Two pointers are maintained to access the list (front and rear) |
| Used in solving problems works on recursion | Used in solving problems having sequential processing |

