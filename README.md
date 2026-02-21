Insert Node at the Beginning of a Singly Linked List (C)

This project contains a C program that demonstrates how to insert a node at the beginning of a singly linked list using functions.

📖 Description

The program:

Defines a Node structure for a singly linked list

Uses dynamic memory allocation (malloc)

Inserts nodes at the beginning of the list

Prints the updated linked list

This example is useful for understanding pointers, dynamic memory allocation, and linked list operations in C.

⚙️ How It Works
🔹 Insertion at Beginning Logic

Create a new node using malloc.

Assign data to the new node.

Set the new node’s next pointer to the current head.

Update the head pointer to the new node.

Since insertion happens at the beginning, the time complexity is:

Time Complexity: O(1)

Space Complexity: O(1)

🖥️ Program Code
#include <stdio.h>
#include <stdlib.h>

// Definition of a node
struct Node {
    int data;
    struct Node* next;
};

// Function to insert a node at the beginning
void insertAtBeginning(struct Node** head, int data) {
    struct Node* newNode = (struct Node*) malloc(sizeof(struct Node));

    newNode->data = data;
    newNode->next = *head;
    *head = newNode;
}

// Function to print the list
void printList(struct Node* head) {
    while (head != NULL) {
        printf("%d -> ", head->data);
        head = head->next;
    }
    printf("NULL\n");
}

// Main function
int main() {
    struct Node* head = NULL;

    // Insert nodes at the beginning
    insertAtBeginning(&head, 10);
    insertAtBeginning(&head, 20);
    insertAtBeginning(&head, 30);

    // Print the list
    printList(head);

    return 0;
}
▶️ How to Run
Step 1: Compile the program
gcc linkedlist.c -o linkedlist
Step 2: Run the program
./linkedlist
📝 Output
30 -> 20 -> 10 -> NULL
🎯 Features

Uses functions for better modularity

Demonstrates pointer-to-pointer (struct Node** head)

Dynamic memory allocation

Clean and beginner-friendly implementation

📚 Author

Ritik Chauhan

If you want, I can also create:

🔹 README with project structure

🔹 Insert at end / delete node program

🔹 Fully menu-driven linked list project 🚀
