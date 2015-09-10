## Out of the box Algorithms provided:
### Apache Spark

- ConnectedComponents: Label Connected components in graph. 
- Label Propagation algorithm
- PageRank algorithm implementation
- Implementation of SVD++ algorithm
- ShortestPaths: Computes shortest paths to the given set of landmark vertices, returning a graph where each vertex attribute is a map containing the shortest-path distance to each reachable landmark
- Strongly connected components
- TriangleCount: Compute the number of triangles passing through each vertex
- In addition to that, there are many third party implementations of various algorithms available.

### STINGER
- Streaming edge insertions and deletions: Performs new edge insertions, updates, and deletions in batches or individually.
- Streaming clustering coefficients: Tracks the local and global clustering coefficients of a graph under both edge insertions and deletions.
- Streaming connected components: Accurately tracks the connected components of a graph with insertions and deletions.
- Streaming community detection: Track and update the community structures within the graph as they change.
- Parallel agglomerative clustering: Find clusters that are optimized for a user-defined edge scoring function.
- Streaming Betweenness Centrality: Find the key points within information flows and structural vulnerabilities.
- K-core Extraction: Extract additional communities and filter noisy high-degree vertices.
- Classic breadth-first search: Performs a parallel breadth-first search of the graph starting at a given source vertex to find shortest paths.



Reference
---------
1. STINGER introduction [link](http://www.stingergraph.com/index.php?id=introduction)
2. GraphX programming guide [link](http://spark.apache.org/docs/latest/graphx-programming-guide.html#graph-operators)
3. GraphX Algorithms [link](http://spark.apache.org/docs/latest/api/scala/index.html#org.apache.spark.graphx.lib.package)
4. Difference between shared memmory (openMp) vs distributed memmory architectures for Big data processing [link](http://www.quora.com/What-are-the-advantages-of-Hadoop-over-openMP)
5. Comparison of various graph processing technologies [link](http://www.stingergraph.com/data/uploads/papers/ppaa2014.pdf)
