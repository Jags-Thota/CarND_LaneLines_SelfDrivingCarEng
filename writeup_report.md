# **Finding Lane Lines on the Road** 

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project we will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.


[//]: # (Image References)

[image1]: ./test_images/solidWhiteCurve.jpg "Solid White Curve - Original Image"
[image2]: ./test_images_output/grayScale_solidWhiteCurve.jpg "Solid White Curve - Gray Scale Image"
[image3]: ./test_images_output/Masked_solidWhiteCurve.jpg "Solid White Curve - Masked"
[image4]: ./test_images_output/CannyEdges_solidWhiteCurve.jpg "Solid White Curve - Canny Edges"
[image5]: ./test_images_output/Lines_solidWhiteCurve.jpg "Solid White Curve - Lines"
[image6]: ./test_images_output/solidWhiteCurve.jpg "Solid White Curve - Output"


---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

### Pipeline
1. Convert Image to Gray Scale image using Open CV library cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)
2. Convert the image to HSV then use color thresholding to identify Yellow lines
3. Apply Guassian filter
4. Generate Canny edges
5. CReate as mask for region of interest
6. Generate Hough lines
7. Combine the original image and the lines to generate final output

Original Image
![image1]
##Convert to Gray Scale Image 
![image2]
##Apply Mask
![image3]
## Canny Edges
![image4]
## Lines
![image5]
## Final Output
![image6]



### 2. Identify potential shortcomings with your current pipeline


One of the shortcomings is detection of teh lines when the image is bright due to sunlight. 


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to smooth the lines. .
