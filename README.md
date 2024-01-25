
# Queue Data Structure Implementation in C

This repository contains a C implementation of a Queue data structure with both array and linked list options. The code provides a menu-driven interface for easy interaction.

## Introduction

This C program implements a Queue data structure, offering users both array and linked list implementations. The menu-driven interface allows easy navigation and interaction with the queue operations.

## Features

- Array and linked list implementations.
- Dynamic memory allocation for linked lists.
- Menu-driven interface for easy interaction.

## File Structure

- `main.c`: Contains the main menu and function implementations.
- `README.md`: Documentation for the project.

## How to Use

1. Compile the program: `gcc main.c -o queue`
2. Run the executable: `./queue`

## Detailed Explanation

### Main Menu

**Algorithm:**
1. Display the main menu options.
2. Read the user's choice.
3. Based on the choice, either call `sub_menu_array()` for array implementation, `sub_menu_linked_list()` for linked list implementation, or exit the program.
4. Handle invalid choices by notifying the user.

### Linked List Implementation

**Algorithms:**

1. **enqueue_linked_list:**
   - Allocate memory for a new node (`temp`).
   - Set the data of `temp` to the given value.
   - Set the next pointer of `temp` to NULL.
   - If the queue is empty (`top == NULL`), set `top` to `temp`.
   - Otherwise, traverse the linked list to find the last node and set its next pointer to `temp`.

2. **dequeue_linked_list:**
   - Check if the queue is empty (`top == NULL`).
   - If not empty, print the data of the node to be removed (`top->data`).
   - Update `top` to point to the next node (deleting from the beginning).

3. **display_linked_list:**
   - Traverse the linked list starting from the `top`.
   - Print the data of each node until reaching the end or an empty list.

### Array Implementation

**Algorithms:**

1. **enqueue_array:**
   - Check for overflow conditions: if the queue is full.
   - If the queue is empty, set both `front` and `rear` to 0 and insert the element.
   - If `rear` is at the end and `front` is not at 0, wrap `rear` around to the beginning.
   - Otherwise, increment `rear` and insert the element.

2. **dequeue_array:**
   - Check for underflow condition: if the queue is empty (`front == -1`).
   - If not empty, print the element at the front (`S[front]`) and increment `front`.

3. **display_array:**
   - Check if the queue is empty (`front == -1`).
   - If not empty, print each element from `front` to `rear`.
