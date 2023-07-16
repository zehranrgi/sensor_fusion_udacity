 
## Lesson 2 Point Cloud Segmentation

What whould be the objects that can be found in the PCD (Point Cloud Data) but are not considered obstacles in our scene?
We can use RANSAC algorithm for it. 

## RANSAC -> Random Sample Consensus

RANSAC is a technique used to identify outliers in data. It operates by randomly selecting subsets of the data and fitting models, such as lines or planes, to these subsets. The iteration that yields the highest number of inliers or the lowest noise is considered the best-fit model. In one variation of RANSAC, the smallest subset of points required to define a model (e.g., two points for a line, three points for a plane) is chosen, and the number of inliers is calculated by measuring the distances between the remaining points and the model. Points within a certain distance to the model are considered inliers. Another variation involves randomly sampling a percentage of the points, fitting a model, and calculating the error. The iteration with the lowest error is deemed the best model. This approach offers the advantage of not having to consider every point in each iteration.



## PCL to Segment Plane

The points that belong to the road from the points that belong to the scene will be seperated with this lesson code. with the ```std::pair```, it will help us to hold our segmented results as obstacle the point cloud and the road point cloud. 

```PointT``` means that it can handle pointxyz, pointrgb or pointxyzi whatever it will take. 


![](https://github.com/zehranrgi/sensor_fusion_udacity/blob/fcdd043b320d5ea3648cf6ddb4ee04941eda7ed7/lesson2/lesson2-ouput.png)
