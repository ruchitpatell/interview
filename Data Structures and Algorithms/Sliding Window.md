## Sliding Window

### General Approach

Define the Window:
- Determine the size of the window (fixed or variable).
- Identify what data structure will represent the window (array, deque, etc.).

Initialize the Window:
- Initialize the window with the first set of elements.
- Perform any initial calculations needed.

Slide the Window:
- Move the window one position to the right.
- Update any data structures or variables that are used to maintain the window's condition.
- Perform any necessary calculations for the new window position.
- (Wrap circular arrays)

Repeat Until End of Data:
- Continue sliding the window until the end of the data set is reached.
- Collect results as needed.

### Problems

1. Medium [1151. Minimum Swaps to Group All 1's Together](https://leetcode.com/problems/minimum-swaps-to-group-all-1s-together/)
