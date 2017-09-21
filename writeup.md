# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**



[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Pipeline

1. Read in and grayscale the image

2. Apply Gaussian Smoothing

3. Apply Canny edge detection

4. Apply an image mask 

5. Apply Hough transform to get lines

6. Based on the line slope, separate the lines into 2 clusters (right and left)

7. Apply Linear Regression to right lines and left lines respectively

8. Draw lines on a blank image

9. Combine the line image with the original image



### 2. Potential shortcomings with the current pipeline

Potential Shortcomings:

1. The performance of the linear regression method depends on the training data. 
That means it is really important to find the points of lane lines with high accuracy.
Poor weather conditions, unclean ground or shadows may cause a worse and unstable performance.





### 3. Suggest possible improvements to your pipeline

A possible improvement would be to delete the outliers when appling linear regression.

Another potential improvement could be to combine with the color detection method.
