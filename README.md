# Adding-Two-Numbers-as-Linked-Lists-

Problem Description
You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order, and each node of the linked list contains a single digit. Your task is to add the two numbers represented by these linked lists and return the sum as a new linked list. The resulting linked list should have its digits stored in reverse order.

**Example:**

Input: (2 -> 4 -> 3) + (5 -> 6 -> 4)
Output: 7 -> 0 -> 8
Explanation: 342 + 465 = 807.

**Solution Approach**
To solve this problem, we can iterate over both linked lists simultaneously, starting from the heads of the lists. We'll add the corresponding digits along with any carry from the previous digit. The sum will be stored in a new linked list node, and the carry will be updated accordingly. If one list is shorter than the other, we can consider the missing digits as 0.

We'll continue this process until we reach the end of both linked lists. Finally, if there's any remaining carry, we'll create a new node with that value.

The algorithm follows these steps:

Initialize a dummy head node and a current node to keep track of the result linked list.
Initialize carry as 0.
Iterate over both linked lists simultaneously, until both lists are empty:
Get the values of the current nodes of both lists. If one list is empty, consider the value as 0.
Calculate the sum of the values along with the carry.
Update the carry as the integer division of the sum by 10.
Create a new node with the remainder of the sum (sum % 10).
Move the current pointer to the next node in the result linked list.
Move both pointers of the input linked lists to their next nodes if they exist.
If there's any remaining carry, create a new node with the carry as its value.
Return the head of the result linked list (excluding the dummy head).
**Complexity Analysis**
The time complexity for this solution is O(max(m, n)), where m and n are the lengths of the two input linked lists. We iterate over both lists simultaneously to calculate the sum.

The space complexity is O(max(m, n)) as well, since we create a new linked list to store the sum. The space required is proportional to the length of the longer input list.

**Summary**
The "Adding Two Numbers as Linked Lists" problem involves adding two non-negative numbers represented by linked lists in reverse order. By iterating over the lists and keeping track of the carry, we can calculate the sum and return it as a new linked list. The solution has a time complexity of O(max(m, n)) and a space complexity of O(max(m, n)).
