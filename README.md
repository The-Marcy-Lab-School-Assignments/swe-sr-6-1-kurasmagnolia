# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

Michael Stawowski: Questions 1 & 2

## Prompt 1

Arrays, Linked Lists and Doubly Linked Lists all allow programmers to organize data in a sequence. So, how would you choose to use one over the other?

In your response, make sure to compare the time complexities for insertion, removal, and random access (grabbing a particular known element by index/position) for each data structure as well as memory usage and ease of traversal.

### Response 1

When deciding whether to choose between arrays, linked lists and doubly linked lists, the decision depends on the operations you prioritize in your algorithm. Arrays provide constant-time random access and are memory efficient due to contiguous allocation, However are inefficient at inserting and remove operations - especially at the head or middle. Which require shifting the elements, therefore making the operations a O(n) time complexity. Single linked lists are efficient at insertions and removals at the head, Although accessing elements by index or insertion in the middle requires traversal i.e O(n) time complexity. Additionally, more memory is required due to pointer overhead. Doubly linked lists go one step further with memory usage by storing both a next and previous pointer thus requiring even more memory. In turn, enabling efficient insertions and deletions at both ends of the list and allowing for bi-directional traversal.

The question remains when to use one over the other, use arrays when fast random access and memory usage matter, Single linked list when you need frequent front-end operations with low memory concerns and doubly linked list when you need additional flexibility with insertion/removals and bi-directional traversal.

## Prompt 2

Imagine you are developing a web browser's "back" button functionality. When a user clicks "back," the browser should navigate to the previously visited webpage.

Would you use a stack or a queue to implement this functionality?

In your response, explain what a Stack/Queue is and why it would be best for this use case. Make sure that your response includes the terms LIFO or FIFO.

### Response 2

The best data structure to implement the "back" feature on a web browser would be a **Stack** because it follows the **LIFO** principle. The stack would store the webpages in the order they were visited with the most recent at the top. So when the user clicks on the "back" button the most recently visited page would be popped of the top.

## Prompt 3

What is an Abstract Data Type and why are they worth learning about?

### Response 3

## Prompt 4

A few classic problems involving a stack are the `isBalanced` and `isPalindrome` functions. Choose one of these functions and provide a solution to it along with a brief lesson explaining how it works.

### Response 4
