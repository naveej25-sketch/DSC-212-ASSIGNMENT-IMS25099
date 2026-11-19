# Modularity on the Karate Club Graph

**DSC212 – Graph Theory Module · Research Assignment**

## What the notebook does
1. Builds the modularity matrix `B = A - k kᵀ / 2m` and checks its properties (symmetry, `B·1 = 0`, `Q = 0` for the trivial partition).
2. Splits a community with the sign of the leading eigenvector of the restricted matrix `B^(C)`, and stops when `λ₁ ≤ 0`.
3. Applies this recursively (recursive bisection) to find multiple communities.
4. Draws the graph after every split (fixed layout, one colour per community, node IDs as labels).
5. After every split computes degree, betweenness, closeness and clustering with NetworkX (inside each node's current community) and plots how each node's value evolves.
6. Discusses which nodes remain central and how community structure influences the metrics.

## Results
| | |
|---|---|
| Splits performed | 4 → 5 communities |
| Final modularity Q | 0.4094 (matches `networkx` modularity) |
| First split vs. real split | 33 of 34 members on the correct side (only node 8 differs) |
| Most consistently central nodes | 0 (Mr. Hi), 33 (president), and 32 |

