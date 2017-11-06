# OpenCV-EC601
  - OpenCV Projects and Exercises

## Exercise 1

**1. How does a program read the cvMat object, in particular, what is the order of the pixel structure?**

The pixel values of a cvMat file can be accessed using _cvMatName.at(x,y)_ where we can access a pixel in the matrix structure where (x,y) is the position of the pixel and (0,0) position is at the top left corner of the matrix.

## Exercise 2

**1. ColorImage.cpp is a program that takes a look at colorspace conversions in OpenCV. Run the code in ColorImage.cpp and comment on the outputs. Implement the same thing in Python and save each image.**

Reading a colored image 'baboon.jpg', and breaking it up into several different colorspaces. We are shown the red, green, and blue intensities of the image. Additionally, we can see the Y, Cr, Cb, Hue, Saturation and value colorspaces. 

**2. Print out the values of the pixel at (20,25) in the RGB, YCbCr and HSV versions of the image. What are the ranges of pixel values in each channel of each of the above mentioned colorspaces?**

- RGB(20,25) = [102,165,156]
- YCRCB(20,25) = [155,129,98]
- HSV(20,25) = [34,97,165]

Pixel values in each channel range from 0-225.

## Exercise 4


