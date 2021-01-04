# K Nearest Neighbors: Spatial Partitioning Data Structures

## TLDR:
Because this was the class' first exposure to DLang, professor Ben Jones provided common.d and dumbknn.d to prevent any unfamiliarity with DLang syntax inhibiting our ability to implement the following algorithms.

## App
Driver file modified to collect performance as a function of N and number of dimensions vs time. Outputs data in a csv file.

## DumbKNN
Code provided by Ben Jones namely to demonstrate DLang syntax and also to provide an example of one (very inefficient) way of KNN analysis. Each query loops through every point in N and calculates distance to query point individually.

## BucketKNN
Divides data set spatially into "buckets".  As opposed to the dumbknn algorithm that searches through all points, this algorithm divides data set into sections so that any query only has to examine the points within a predetermined range (the bounds of the buckets). Ideal for data that are fairly evenly distributed.

## QuadTree
A tree spatial partitioning data structure that recursively divides data into quadrants until one data point per quadrant (there some quadrants might have no points. Wikipedia has more detailed information about [quad tress](https://en.wikipedia.org/wiki/Quadtree). Implementation for 2D data only.

## KDTree
Another tree spatial partitioning data structure that recursively divides data at the median for each dimension for N dimensions. Again, Wikipedia has more detailed information about [KD trees](https://en.wikipedia.org/wiki/K-d_tree).

### Disclaimer:
Skeleton code written by Ben Jones and includes dumbknn.d, common.d, and parts of app.d
