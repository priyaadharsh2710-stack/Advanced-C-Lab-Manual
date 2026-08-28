EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    char data;
    struct node *next;
};

void search(struct node *head, char key)
{
    struct node *temp = head;
    int found = 0;

    while (temp != NULL)
    {
        if (temp->data == key)
        {
            found = 1;
            break;
        }

        temp = temp->next;
    }

    if (found == 1)
    {
        printf("Element %c found in the linked list", key);
    }
    else
    {
        printf("Element %c not found in the linked list", key);
    }
}

int main()
{
    struct node *head;
    struct node *second;
    struct node *third;

    head = (struct node *)malloc(sizeof(struct node));
    second = (struct node *)malloc(sizeof(struct node));
    third = (struct node *)malloc(sizeof(struct node));

    head->data = 'A';
    head->next = second;

    second->data = 'B';
    second->next = third;

    third->data = 'C';
    third->next = NULL;

    search(head, 'B');

    return 0;
}
```

Output:

<img width="741" height="153" alt="image" src="https://github.com/user-attachments/assets/37b0760e-7751-49ac-9d77-53c29053af8f" />




Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    char data;
    struct node *next;
};

struct node *insert(struct node *head, char value)
{
    struct node *newnode;
    struct node *temp;

    newnode = (struct node *)malloc(sizeof(struct node));

    newnode->data = value;
    newnode->next = NULL;

    if (head == NULL)
    {
        head = newnode;
    }
    else
    {
        temp = head;

        while (temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newnode;
    }

    return head;
}

void display(struct node *head)
{
    struct node *temp = head;

    printf("Linked list elements are:\n");

    while (temp != NULL)
    {
        printf("%c ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    struct node *head = NULL;

    head = insert(head, 'A');
    head = insert(head, 'B');
    head = insert(head, 'C');

    display(head);

    return 0;
}
```
Output:

<img width="740" height="170" alt="image" src="https://github.com/user-attachments/assets/4c75d63b-25b3-4e86-8f05-40c6639ff082" />


 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    char data;
    struct node *prev;
    struct node *next;
};

void traverse(struct node *head)
{
    struct node *temp = head;

    printf("Doubly linked list elements are:\n");

    while (temp != NULL)
    {
        printf("%c ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    struct node *head;
    struct node *second;
    struct node *third;

    head = (struct node *)malloc(sizeof(struct node));
    second = (struct node *)malloc(sizeof(struct node));
    third = (struct node *)malloc(sizeof(struct node));

    head->data = 'A';
    head->prev = NULL;
    head->next = second;

    second->data = 'B';
    second->prev = head;
    second->next = third;

    third->data = 'C';
    third->prev = second;
    third->next = NULL;

    traverse(head);

    return 0;
}
```
Output:

<img width="741" height="167" alt="image" src="https://github.com/user-attachments/assets/b359901c-628f-4441-b630-907155e2c9f8" />



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    char data;
    struct node *prev;
    struct node *next;
};

struct node *insert(struct node *head, char value)
{
    struct node *newNode;
    struct node *temp;

    newNode = (struct node *)malloc(sizeof(struct node));

    newNode->data = value;
    newNode->prev = NULL;
    newNode->next = NULL;

    if (head == NULL)
    {
        head = newNode;
    }
    else
    {
        temp = head;

        while (temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newNode;
        newNode->prev = temp;
    }

    return head;
}

void display(struct node *head)
{
    struct node *temp = head;

    printf("Doubly linked list elements are:\n");

    while (temp != NULL)
    {
        printf("%c ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    struct node *head = NULL;

    head = insert(head, 'A');
    head = insert(head, 'B');
    head = insert(head, 'C');

    display(head);

    return 0;
}
```

Output:

<img width="742" height="178" alt="image" src="https://github.com/user-attachments/assets/79b664ab-e890-408d-b105-07f89385d3dc" />



Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    char data;
    struct node *next;
};

struct node *delete(struct node *head, char value)
{
    struct node *temp;
    struct node *prev;

    if (head == NULL)
    {
        printf("Linked list is empty");
        return head;
    }

    if (head->data == value)
    {
        temp = head;
        head = head->next;
        free(temp);

        printf("Element %c deleted\n", value);
        return head;
    }

    prev = head;
    temp = head->next;

    while (temp != NULL)
    {
        if (temp->data == value)
        {
            prev->next = temp->next;
            free(temp);

            printf("Element %c deleted\n", value);
            return head;
        }

        prev = temp;
        temp = temp->next;
    }

    printf("Element %c not found in the linked list\n", value);

    return head;
}

void display(struct node *head)
{
    struct node *temp = head;

    printf("Linked list elements are:\n");

    while (temp != NULL)
    {
        printf("%c ", temp->data);
        temp = temp->next;
    }
}

int main()
{
    struct node *head;
    struct node *second;
    struct node *third;

    head = (struct node *)malloc(sizeof(struct node));
    second = (struct node *)malloc(sizeof(struct node));
    third = (struct node *)malloc(sizeof(struct node));

    head->data = 'A';
    head->next = second;

    second->data = 'B';
    second->next = third;

    third->data = 'C';
    third->next = NULL;

    head = delete(head, 'B');

    display(head);

    return 0;
}
```
Output:

<img width="740" height="197" alt="image" src="https://github.com/user-attachments/assets/37182dcf-f69b-4d2b-94dc-b0dea0affe1b" />



Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





