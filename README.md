# Computer-Vision-blobDetection

Scale-space blob detection
To detect blobs at multiple scales, there are two strategies to complete the task: 
(1) iteratively filter the image with kernel of increasing size. 
(2) iteratively downsample the image and filter it with the kernel of fixed size. Upsample the result or do some interpolation in order to find maxima in scale space for the
second approach. Approach two is faster as compared to approach 1.

Approach 1:

1. Build a Laplacian scale space, starting with some initial scale and going for n iterations:
* Filter image with scale-normalized Laplacian at current scale.
*  Save the square of Laplacian response for current level of scale space.
* Increase scale by a factor k.
2. Perform non-maximum suppression in scale space.
3. Display resulting circles at their characteristic scales for points above a threshold.


Download this folder and execute evalblobDetection to detect blobs. To see the difference between approach 1 and approach 2. Modify the flag in detectblobs.m file.
