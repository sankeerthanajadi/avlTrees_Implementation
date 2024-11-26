# avlTrees_Implementation

1. Binary Search Trees (BST) and Their Time Complexity for Key Operations
   
A Binary Search Tree (BST) is a hierarchical data structure where:
Each node has at most two children, designated as the left and right child.
The key in each node satisfies the following properties:
Keys in the left subtree are less than or equal to the node's key.
Keys in the right subtree are greater than or equal to the node's key.
Time Complexity
The efficiency of key operations in a BST depends on the tree's height (ℎ):
Search: 𝑂(ℎ)
In the worst case (when the tree is skewed), ℎ=𝑛, making the time complexity 𝑂(𝑛)
where 𝑛 is the number of nodes.
Insert: 𝑂(ℎ) as the process involves traversing the tree to find the correct position.
Delete: 𝑂(ℎ) since deletion may involve finding the node and restructuring the tree.
Challenge
When a BST becomes unbalanced (e.g., skewed), its height approaches 𝑛 leading to degraded performance.

2. The Need for Self-Balancing Trees
To address the potential inefficiency of unbalanced BSTs, self-balancing trees, such as AVL and Red-Black trees, are employed. These trees maintain a balanced structure, ensuring that the height of the tree remains logarithmic relative to the number of nodes.

Advantages of Self-Balancing Trees:
Optimal Time Complexity: They ensure 𝑂(log 𝑛)
for search, insert, and delete operations by keeping the height of the tree proportional to O(log 𝑛)
Consistent Performance: Prevent performance degradation caused by unbalanced trees.

3. Introduction to AVL Trees and Detecting Imbalance
An AVL Tree (named after its inventors Adelson-Velsky and Landis) is a type of self-balancing BST that enforces balance using a property called the balance factor.

Balance Factor
The balance factor of a node is defined as:
Balance Factor=Height of Left Subtree − Height of Right Subtree
A node is considered balanced if its balance factor is in the range [−1,1].
If the balance factor is outside this range, the tree becomes imbalanced and requires rebalancing.

4. Imbalance Cases in AVL Trees (LL, LR, RL, RR)
When an AVL tree becomes imbalanced, it falls into one of four cases:

LL (Left-Left): The left child of the left subtree is too heavy.
LR (Left-Right): The right child of the left subtree is too heavy.
RL (Right-Left): The left child of the right subtree is too heavy.
RR (Right-Right): The right child of the right subtree is too heavy.

5. Rebalancing AVL Trees
To restore balance, AVL trees use rotations:

LL Case: Perform a right rotation at the imbalanced node.
LR Case: Perform a left rotation at the left child, followed by a right rotation at the imbalanced node.
RL Case: Perform a right rotation at the right child, followed by a left rotation at the imbalanced node.
RR Case: Perform a left rotation at the imbalanced node.
These rotations maintain the BST property while minimizing the height.

6. AVL Trees vs. Red-Black Trees: When to Use Each?
Both AVL and Red-Black trees are self-balancing BSTs, but they are optimized for different scenarios:

AVL trees:
  More balanced than Red-Black trees, which leads to faster search times.
  More complex to implement and maintain.
  Suitable for applications where search is the most frequent operation.
Red-Black trees:
  Less balanced than AVL trees, but still provide good performance.
  Easier to implement and maintain than AVL trees.
  Suitable for applications where insert and delete operations are frequent.
