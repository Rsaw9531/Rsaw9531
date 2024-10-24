- 👋 Hi, I’m @Rsaw9531
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
#include <stdio.h>

#include <stdlib.h>

struct Node

{

int data;

struct Node* next;

};

struct Node* create_node(int data)

{

struct Node* new_node = (struct Node*)malloc(sizeof(struct Node));

new_node->data = data;

new_node->next = NULL;

return new_node;

}

void insert_at_beginning(struct Node** head, int data) {

struct Node* new_node = create_node(data);

new_node->next = *head;

*head = new_node;

}

void delete_from_end(struct Node** head) {

if (*head == NULL)

{

printf("List is empty, nothing to delete.\n");

return;

}

struct Node* temp = *head;

if (temp->next == NULL) {

free(temp);

*head = NULL;

return;

}

while (temp->next->next != NULL) {

temp = temp->next;

}

free(temp->next);temp->next = NULL;

}

void traverse(struct Node* head) {

struct Node* current = head;

if (current == NULL) {

printf("List is empty.\n");

return;

}

printf("Linked List: ");

while (current != NULL) {

printf("%d -> ", current->data);

current = current->next;

}

printf("NULL\n");

}

int main(void)

{

struct Node* head = NULL;

int choice, data;

while (1)

{

printf("\nMenu:\n");

printf("1. Insert at Beginning\n");

printf("2. Delete from End\n");

printf("3. Traverse\n");

printf("4. Exit\n");

printf("Enter your choice: ");

scanf("%d", &choice);

switch (choice)

{

case 1:

printf("Enter data to insert at beginning: ");

scanf("%d", &data);

insert_at_beginning(&head, data);

break;

case 2:delete_from_end(&head);

break;

case 3:

traverse(head);

break;

case 4:

printf("Exiting...\n");

exit(0);

default:

printf("Invalid choice! Please try again.\n");

}

}

return 0;

}#include <stdio.h>

#include <stdlib.h>

struct Node

{

int data;

struct Node* next;

};

struct Node* create_node(int data)

{

struct Node* new_node = (struct Node*)malloc(sizeof(struct Node));

new_node->data = data;

new_node->next = NULL;

return new_node;

}

void insert_at_beginning(struct Node** head, int data) {

struct Node* new_node = create_node(data);

new_node->next = *head;

*head = new_node;

}

void delete_from_end(struct Node** head) {

if (*head == NULL)

{

printf("List is empty, nothing to delete.\n");

return;

}

struct Node* temp = *head;

if (temp->next == NULL) {

free(temp);

*head = NULL;

return;

}

while (temp->next->next != NULL) {

temp = temp->next;

}

free(temp->next);temp->next = NULL;

}

void traverse(struct Node* head) {

struct Node* current = head;

if (current == NULL) {

printf("List is empty.\n");

return;

}

printf("Linked List: ");

while (current != NULL) {

printf("%d -> ", current->data);

current = current->next;

}

printf("NULL\n");

}

int main(void)

{

struct Node* head = NULL;

int choice, data;

while (1)

{

printf("\nMenu:\n");

printf("1. Insert at Beginning\n");

printf("2. Delete from End\n");

printf("3. Traverse\n");

printf("4. Exit\n");

printf("Enter your choice: ");

scanf("%d", &choice);

switch (choice)

{

case 1:

printf("Enter data to insert at beginning: ");

scanf("%d", &data);

insert_at_beginning(&head, data);

break;

case 2:delete_from_end(&head);

break;

case 3:

traverse(head);

break;

case 4:

printf("Exiting...\n");

exit(0);

default:

printf("Invalid choice! Please try again.\n");

}

}

return 0;

}
<!---
Rsaw9531/Rsaw9531 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
