## Graph

- Breath First Search

- Depth First Search

- Strongly Connected Components

- Union-Find (Disjoint Set, Path Compression, Union by Rank)
    - Disjoint Set
        - find(x): Returns the representative of the group (root)
            - travel upwards until we find the root
            - stop when root (parent root == root)
        - union(a, b): Unions the representative of two trees (unoptimized)
            - set root of one tree (smaller) to be child of another
        - Time O(log n), Space O(n)

        - Pseudocode:
            - find(x):
                ```python
                if parent[x] == x:
                    return x
                return find(parent[x])
                ```
            - union(a, b):
                ```python
                parent[find(parent[a])] = find(parent[b])
                ```

    - Path Compression (find) + Rank (union)
        - find(x): every time we want to find, set the parent to root most node
        - Pseudocode:
            - find(x):
                ```python
                if parent[x] != x:
                    parent[x] = find(parent[x])
                return parent[x]
                ```

        - union(x): attach smaller tree into deeper one, increase height/rank
        - Pseudocode:
            - def union(a, b): 
                ```python
                rootA = find(a)
                rootB = find(b)
                if rootA != rootB: 
                    if rank[rootA] > rank[rootB]: 
                        parent[rootB] = rootA 
                    elif rank[rootA] < rank[rootB]:
                        parent[rootA] = rootB
                    else: 
                        parent[rootB] = rootA   // rootA’s deeper
                        rank[rootA] += 1
                ```

    1. Easy [1971. Find if Path Exists in Graph](https://leetcode.com/problems/find-if-path-exists-in-graph/)
    2. Medium [1061. Lexicographically Smallest Equivalent String](https://leetcode.com/problems/lexicographically-smallest-equivalent-string/)

- Topological Sort

- Minimum Spanning Tree

- Single Point Shortest Path (Dijkstra’s, Prim’s, Bellman-Ford)

- All-pairs Shortest Path
    - Floyd-Warshall
        - Shortest path between all pairs of vertices. Negative edges allowed.
        - Time: O(V^3), Space: O(V^2).

        - Challenges
            - Medium [1334. Find the City With the Smallest Number of Neighbors at a Threshold Distance](https://leetcode.com/problems/find-the-city-with-the-smallest-number-of-neighbors-at-a-threshold-distance/description/)
