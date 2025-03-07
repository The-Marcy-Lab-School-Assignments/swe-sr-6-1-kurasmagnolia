<!-- @format -->

# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Arrays, Linked Lists and Doubly Linked Lists all allow programmers to organize data in a sequence. So, how would you choose to use one over the other?

In your response, make sure to compare the time complexities for insertion, removal, and random access (grabbing a particular known element by index/position) for each data structure as well as memory usage and ease of traversal.

### Response 1

## Prompt 2

Imagine you are developing a web browser's "back" button functionality. When a user clicks "back," the browser should navigate to the previously visited webpage.

Would you use a stack or a queue to implement this functionality?

In your response, explain what a Stack/Queue is and why it would be best for this use case. Make sure that your response includes the terms LIFO or FIFO.

### Response 2

## Prompt 3

What is an Abstract Data Type and why are they worth learning about?

### Response 3

An Abstract Data Type (ADT) is like a blueprint for a data structure—it tells you what you can do with the data but not how it's actually done behind the scenes. It’s all about focusing on the operations rather than the specific implementation.

Learning about ADTs is super useful because they help you think through algorithms, show up in real-world applications (like databases and networking), and let you focus on solving problems without getting stuck on the details. Some common ADTs you might run into are stacks, queues, and graphs, which are essential in programming and software development.

## Prompt 4

A few classic problems involving a stack are the `isBalanced` and `isPalindrome` functions. Choose one of these functions and provide a solution to it along with a brief lesson explaining how it works.

### Response 4

How the `isBalanced` function below "isBalancedParentheses" works that it verifies whether pairs of parentheses in a given input string (`inputString`) are correctly matched with one another. It uses a stack data structure, where we use an array to implement it, to keep track of opening brackets '(' by adding them to the stack, and checks if they have corresponding closing brackets in the correct order.

#### How it works step-by-step:

- Opening Bracket: If an opening bracket is encountered, it is pushed onto the stack.
- Closing Bracket: If a closing bracket is encountered, the algorithm checks:
  - If the stack is empty, it means there's no matching opening bracket, and the string is unbalanced.
  - If the stack is not empty, the top element (last added opening bracket) is popped.
  - If the popped opening bracket does not match the current closing bracket, the string is unbalanced.

* Final Check: After processing the entire string, if the stack is empty, it means all brackets were balanced. If the stack is not empty, it means there are unmatched opening brackets, and the string is unbalanced.

Code Snippet:

```JavaScript
// Stack class created implementing an array to replicate it
class Stack {
  stack = [];

  push(data) {
    this.stack.push(data); // .push() method = constant | .unshift() method = linear (we don't want that)
  }

  pop() {
    return this.stack.pop(); // .pop() method does 2 things: removes the element from the end, and returns it to us
  }

  peek() {
    return this.stack[this.stack.length - 1];
  }

  isEmpty() {
    return this.stack.length === 0;
  }

  getSize() {
    return this.stack.length;
  }
}


const isBalancedParentheses = (inputString) => {
  const parenthesesStack = new Stack(); // initialize a new Stack

  for (const parenthesis of inputString) {
    if (parenthesis === '(') {
      // if the current element is an opening...
      parenthesesStack.push(parenthesis); // push it to the Stack
    } else if (!parenthesesStack.isEmpty()) {
      // else if the element is a closing and it's not empty...
      parenthesesStack.pop(); // it will pop an opening out from the stack
    } else {
      return false; // else it will return false since it's on a closing and the Stack is empty
    }
  }
  return parenthesesStack.isEmpty(); // return whether it's balanced or not (true/false)
};
```
