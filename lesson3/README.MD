
If you need to identify and categorize obstacle points for your vehicle, segmenting and grouping them becomes crucial, especially when performing multi-object tracking involving cars, pedestrians etc. One effective method for clustering point cloud data is known as euclidean clustering.

Question to them: 

Do you segment out the ground plane? 
Yes, we segment out the ground plane because to know the height of the above the ground. 

Do hills affect lidar? 
No. 


Clustering 
- group points how they re close and
- KD-tree speeds up closest neighbor search 


## Euclidean Cluster on KD-Tree method


Clustering involves grouping points based on their proximity, and using a KD-Tree can accelerate the search for the nearest neighbors. Euclidean clustering is one approach to group and cluster point cloud data. To efficiently perform a nearest neighbor search, a KD-Tree data structure is utilized, which significantly reduces the lookup time from O(n) to an average of O(log(n)). The KD-Tree partitions the search space, allowing for more efficient identification of nearby points. By organizing points into regions within the KD-Tree, unnecessary distance calculations for thousands of points can be avoided, as they are known to be located outside the considered proximity region.



A KD-Tree is a binary tree structure used for organizing points by splitting regions along alternating axes. It is particularly beneficial when performing tasks such as nearest neighbor search and euclidean clustering. In the context of this quiz, we will focus on a 2D example, where the KD-Tree will be referred to as a 2D-Tree. By partitioning space through axis-based splits, the KD-Tree enables faster and more efficient retrieval of nearest neighbors.

## Bounding Box: 

Box box = pointProcessor->BoundingBox(cluster);
renderBox(viewer,box,clusterId);


Bbox defines the boundaries within which the car is not allowed to enter, as doing so would result in a collision. By staying outside of the bounding box volume, the car ensures safe navigation and avoids potential accidents.
