# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps. First, I converted the images to grayscale, then I define a kernel size and apply Gaussian smoothing, after that define our parameters for Canny and apply to finde the edges, then define a quadrilateral region of interest, make a mask to finde the edges in the rigion, then define the Hough transform parameters and apply to finde the lines,then use draw_lines() to draw lines on the blank image, at last use Weighted_image() to  addweighte the lines image and  the initial image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by average/extrapolate the line segments  detected to map out the full extent of the lane

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming is can't finde the lane accurately at the biger turn. 

Another shortcoming is that sometime long Lane break may confuse the current pipeline and can't get appropriate result. 


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to draw curve lane at biger turn.

Another potential improvement could be to use another lane when one of the lane have long break, beacause the the distance between the two lines is equal.

