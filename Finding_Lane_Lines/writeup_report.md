# **Finding Lane Lines on the Road** 

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


---

### Reflection

### 1. Describe your pipeline.
In this part, we take the image below as the input, and the pipeline method is described in the following steps:

<img width="960" src="https://github.com/ttungl/Self-Driving-Car-ND-term-1/blob/master/Finding_Lane_Lines/test_images/solidYellowCurve.jpg">
Figure 1: Original image.

We convert the original image to the grayscale image as in Figure 2 below:
<img width="960" src="https://github.com/ttungl/Self-Driving-Car-ND-term-1/blob/master/Finding_Lane_Lines/test_images_out/blur_gray_lines.jpg">
Figure 2: Gaussian Smoothing.

<img width="960" src="https://github.com/ttungl/Self-Driving-Car-ND-term-1/blob/master/Finding_Lane_Lines/test_images_out/canny_edges_lines.jpg">
Figure 3: Canny edges detection.

<img width="960" src="https://github.com/ttungl/Self-Driving-Car-ND-term-1/blob/master/Finding_Lane_Lines/test_images_out/masked_edges_region_interest.jpg">
Figure 4: Masked edges region of interest.

<img width="960" src="https://github.com/ttungl/Self-Driving-Car-ND-term-1/blob/master/Finding_Lane_Lines/test_images_out/hough_lines.jpg">
Figure 5: Hough transform on the edges detection of the image.

### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
