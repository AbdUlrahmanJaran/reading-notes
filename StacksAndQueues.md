# Stacks and Queues
## Stack
What is a Stack?
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack.
Stacks follow these concepts:

**FILO**
First In Last Out
This means that the first item added in the stack will be the last item popped out of the stack.

**LIFO**
Last In First Out
This means that the last item added to the stack will be the first item popped out of the stack.

Common terminology for a stack:
1. Push O(1) - Nodes or items that are put into the stack are pushed.<br>
Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in the stack.

2. Pop O(1) - Nodes or items that are removed from the stack are popped.<br>
When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.
3. Top - This is the top of the stack.
4. Peek O(1) - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
5. IsEmpty O(1) - returns true when stack is empty otherwise returns false.

## Queue
What is a Queue?
Queue is a data structure, similar to Stacks but unlike stacks, a queue is open at both its ends. One end is always used to insert data (enqueue) and the other is used to remove data (dequeue).[ref](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)

Queues follow these concepts:
**FIFO**
First In First Out
This means that the first item in the queue will be the first item out of the queue.

**LILO**
Last In Last Out
This means that the last item in the queue will be the last item out of the queue.

Common terminology for a queue:
1. Enqueue O(1) - Nodes or items that are added to the queue.
2. Dequeue O(1) - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
3. Front - This is the front/first Node of the queue.
4. Rear - This is the rear/last Node of the queue.
5. Peek O(1) - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
6. IsEmpty O(1) - returns true when queue is empty otherwise returns false.

### [Ref](https://codefellows.github.io/common_curriculum/data_struct)