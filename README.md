# Distance-between-closest-pair-of-2D-points
The divide and conquer approach to finding the closest pair of 2D points involves the following steps:

Divide the points into two groups by partitioning the space with a vertical line passing through the center of the given points. This can be done by finding the midpoint of the x-coordinates of all the points and drawing a vertical line through this point to separate the points into two groups.

Find the distance between closest pair in each group. This can be done recursively by applying the same algorithm to each group. If there are only two points in a group, we can calculate the distance between them using the direct formula and stop the recursion. If there is only one point in a group, we cannot calculate the distance and return Infinity (a very large value).

There may be some points across the vertical boundary which may be closer than the minimum distance d found above. To check for this, we take a narrow region covering distance d on each side of the vertical boundary set up in step 1, and find the distance between the closest pair of points in this strip. If this distance is smaller than the d calculated above, then this will be the new value of d.
