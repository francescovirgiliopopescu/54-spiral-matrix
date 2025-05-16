# 54-spiral-matrix

Given an m x n matrix, return all elements of the matrix in spiral order.

Input: matrix = [[1,2,3],[4,5,6],[7,8,9]]
Output: [1,2,3,6,9,8,7,4,5]

Input: matrix = [[1,2,3,4],[5,6,7,8],[9,10,11,12]]
Output: [1,2,3,4,8,12,11,10,9,5,6,7]

Constraints:

m == matrix.length
n == matrix[i].length
1 <= m, n <= 10
-100 <= matrix[i][j] <= 100

Solutions

Solution 1: Simulation

We use i and j to represent the row and column of the current element, use k to represent the current direction, and use an array or hash table vis to record whether each element has been visited. Each time we visit an element, we mark it as visited, then move forward in the current direction. If we find that it is out of bounds or has been visited after moving forward, we change the direction and continue to move forward until the entire matrix is traversed.

The time complexity is O(m _ n), and the space complexity is O(m _ n). Here, m and n are the number of rows and columns of the matrix, respectively.

For visited elements, we can also add a constant 300 to their values, so we don’t need an extra vis array or hash table to record whether they have been visited, thereby reducing the space complexity to O(1).

Solution 2: Layer-by-layer Simulation

We can also traverse and store the matrix elements from the outside to the inside, layer by layer.

The time complexity is O(m \* n), and the space complexity is O(1). Here, m and n are the number of rows and columns of the matrix, respectively.
