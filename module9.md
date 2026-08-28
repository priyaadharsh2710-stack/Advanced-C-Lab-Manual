EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

```
#include <stdio.h>

float stack[100];
int top = -1;

void display()
{
    int i;

    if (top == -1)
    {
        printf("Stack is empty");
    }
    else
    {
        printf("Stack elements are:\n");
        for (i = top; i >= 0; i--)
        {
            printf("%.2f ", stack[i]);
        }
    }
}

int main()
{
    stack[0] = 10.5;
    stack[1] = 20.5;
    stack[2] = 30.5;
    top = 2;

    display();

    return 0;
}
 ```

Output:

<img width="742" height="188" alt="image" src="https://github.com/user-attachments/assets/387ed737-69ec-4862-b377-9c6468146a5d" />




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```
#include <stdio.h>

float stack[100];
int top = -1;

void push(float value)
{
    if (top == 99)
    {
        printf("Stack Overflow");
    }
    else
    {
        top++;
        stack[top] = value;
        printf("%.2f pushed into stack\n", value);
    }
}

int main()
{
    push(10.5);
    push(20.5);
    push(30.5);

    return 0;
}
```

Output:

<img width="741" height="217" alt="image" src="https://github.com/user-attachments/assets/e6fa7a3a-a144-47ad-9b62-1e5be055eb01" />




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
#include <stdio.h>

int queue[100];
int front = -1;
int rear = -1;

void display()
{
    int i;

    if (front == -1 || front > rear)
    {
        printf("Queue is empty");
    }
    else
    {
        printf("Queue elements are:\n");

        for (i = front; i <= rear; i++)
        {
            printf("%d ", queue[i]);
        }
    }
}

int main()
{
    queue[0] = 10;
    queue[1] = 20;
    queue[2] = 30;

    front = 0;
    rear = 2;

    display();

    return 0;
}
```

Output:

<img width="741" height="162" alt="image" src="https://github.com/user-attachments/assets/4873b077-b330-4b62-9a57-3dbf638c08c7" />


Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

```
#include <stdio.h>

float queue[100];
int front = -1;
int rear = -1;

void enqueue(float value)
{
    if (rear == 99)
    {
        printf("Queue is full");
    }
    else
    {
        if (front == -1)
        {
            front = 0;
        }

        rear++;
        queue[rear] = value;

        printf("%.2f inserted into queue\n", value);
    }
}

int main()
{
    enqueue(10.5);
    enqueue(20.5);
    enqueue(30.5);

    return 0;
}
```

Output:
<img width="740" height="227" alt="image" src="https://github.com/user-attachments/assets/5709d06f-c483-4145-a13a-ed47118b939c" />


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

```
#include <stdio.h>

float queue[100];
int front = -1;
int rear = -1;

void enqueue(float value)
{
    if (rear == 99)
    {
        printf("Queue is full\n");
    }
    else
    {
        if (front == -1)
        {
            front = 0;
        }

        rear++;
        queue[rear] = value;
    }
}

void dequeue()
{
    if (front == -1)
    {
        printf("Queue is empty\n");
    }
    else
    {
        printf("%.2f deleted from queue\n", queue[front]);
        front++;

        if (front > rear)
        {
            front = -1;
            rear = -1;
        }
    }
}

int main()
{
    enqueue(10.5);
    enqueue(20.5);
    enqueue(30.5);

    dequeue();
    dequeue();

    return 0;
}
```

Output:

<img width="740" height="186" alt="image" src="https://github.com/user-attachments/assets/f32faee5-217d-4c09-94a3-149ada6cfca2" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
