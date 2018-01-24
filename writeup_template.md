# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_image_out/gray_image.png "Grayscale"
[image2]: ./test_image_out/blur_image.png "Gaussian blur"
[image3]: ./test_image_out/edge_image.png "Canny edge detector"
[image4]: ./test_image_out/mask_test.png "Mask image"
[image5]: ./test_image_out/mask_image.png "Mask image"
[image6]: ./test_image_out/line_image.png "Line image"
[image7]: ./test_image_out/add_image.png "Weighted images"
[image8]: ./test_image_out/image_out.png "final output"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

#### My pipeline consisted of 6 step.

1. Grayscale - The original image is 3 channel, this function turn it into 1 channel.
![alt text][image1]

2. Gaussian blur - Run Gaussian smoothing, before running Canny will get better effect. Here I set the mask (5, 5).
![alt text][image2]

3. Canny edge detector - A method of edge detection.
![alt text][image3] ![alt text][image4]

4. Mask image - Remove unuseful areas.
![alt text][image5]

5. Line image - Using cv.HoughLinesP and cv.line function to draw line.
![alt text][image6]

6. Weighted images - Add two images together (one is or original image and anther is line image)
![alt text][image7]


#### In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

### Start at here
![alt text][image8]



### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...