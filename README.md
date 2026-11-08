# Task 2: Singly Linked List

*Module:* KH5002CMD Advanced Algorithms
*Language:* C++ (C++17)

## Description
This project implements a singly linked list in C++ from scratch, without std::list or std::forward_list. The LinkedList class stores integers in nodes that each point to the next node, and it supports insertion at the head and tail, deletion by value, search, length, reversal and printing. A destructor frees every node when the list is destroyed.

## Files
| File | Purpose |
|---|---|
| LinkedList.h | LinkedList class (with its nested Node class) |
| main.cpp | Test driver (TC1 to TC10) |

## Operations
| Operation | Description | Time complexity |
|---|---|---|
| insertAtHead(value) | Adds a node at the front | O(1) |
| insertAtTail(value) | Adds a node at the end | O(n) |
| deleteValue(value) | Removes the first node holding the value; returns true if found | O(n) |
| search(value) | Returns true if the value is in the list | O(n) |
| length() | Returns the number of nodes | O(n) |
| reverse() | Reverses the list in place | O(n) |
| print() | Prints the list as 10->20->NULL | O(n) |

All operations use O(1) extra space.

## Build and run

g++ -std=c++17 main.cpp -o linked_list
./linked_list

On Windows, run linked_list.exe instead of ./linked_list.

## Test cases
The driver runs ten test cases covering insertion at both ends, deletion from the head, tail and middle, a failed deletion, reversal, and operations on an empty list.

| Test | Operation | Expected output |
|---|---|---|
| TC1 | insertAtHead 30, 20, 10 | 10->20->30->NULL |
| TC2 | insertAtTail 40, 50 | 10->20->30->40->50->NULL |
| TC3 | length | length = 5 |
| TC4 | search(30), search(99) | search(30)=1 search(99)=0 |
| TC5 | delete head (10) | 20->30->40->50->NULL |
| TC6 | delete tail (50) | 20->30->40->NULL |
| TC7 | delete middle (30) | 20->40->NULL |
| TC8 | delete missing value (99) | deleteValue(99)=0 |
| TC9 | reverse 1, 2, 3 | 3->2->1->NULL |
| TC10 | operations on an empty list | length=0 search=0 delete=0 |
