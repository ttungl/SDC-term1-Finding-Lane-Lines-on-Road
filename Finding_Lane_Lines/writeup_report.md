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

We apply the Canny edges detection algorithm to extract the edges of the Gaussian Smoothing image, we still keep the low threshold and high threshold at 50 and 150 as recommended, respectively. Note, I have tried to change these values, but the videos have been crashed when running for some reasons. 
<img width="960" src="https://github.com/ttungl/Self-Driving-Car-ND-term-1/blob/master/Finding_Lane_Lines/test_images_out/canny_edges_lines.jpg">
Figure 3: Canny edges detection.

We then mask the trapezoid shape (region of interest) to the image above to use for identifying the lane lines. I have found that the best combination for the hough transform parameters is as follows: rho = 1; theta = (2* np.pi / 180); threshold = 20; min_line_length = 5; and max_line_gap = 20; 
<img width="960" src="https://github.com/ttungl/Self-Driving-Car-ND-term-1/blob/master/Finding_Lane_Lines/test_images_out/masked_edges_region_interest.jpg">
Figure 4: Masked edges region of interest.

For the draw lines function, we calculate the slope and the upper bound of the lines for both sides. Then we draw the lines based on the resulted points on left line and right line. 
<img width="960" src="https://github.com/ttungl/Self-Driving-Car-ND-term-1/blob/master/Finding_Lane_Lines/test_images_out/hough_lines.jpg">
Figure 5: Hough transform on the edges detection of the image.

Finally, we merge the output of the hough transform image with the original image, the result is as below.
<img width="960" src="https://github.com/ttungl/Self-Driving-Car-ND-term-1/blob/master/Finding_Lane_Lines/test_images_out/solidYellowCurve_modified.jpg">



### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
