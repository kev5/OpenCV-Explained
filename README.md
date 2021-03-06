# OpenCV Explained
  - OpenCV Projects and Exercises

Note: All the program codes and results are in the respective folders in the repository. 
## Exercise 1

**1. How does a program read the cvMat object, in particular, what is the order of the pixel structure?**

- The pixel values of a cvMat file can be accessed using _cvMatName.at(x,y)_ where we can access a pixel in the matrix structure where (x,y) is the position of the pixel and (0,0) position is at the top left corner of the matrix.

## Exercise 2

**1. ColorImage.cpp is a program that takes a look at colorspace conversions in OpenCV. Run the code in ColorImage.cpp and comment on the outputs. Implement the same thing in Python and save each image.**

- Reading a colored image 'baboon.jpg', and breaking it up into several different colorspaces. We are shown the red, green, and blue intensities of the image. Additionally, we can see the Y, Cr, Cb, Hue, Saturation and value colorspaces. 

**2. Print out the values of the pixel at (20,25) in the RGB, YCbCr and HSV versions of the image. What are the ranges of pixel values in each channel of each of the above mentioned colorspaces?**

- RGB(20,25) = [102,165,156]
- YCRCB(20,25) = [155,129,98]
- HSV(20,25) = [34,97,165]

  Pixel values in each channel range from 0-225.

## Exercise 3

**1. Look at the code in Noise.cpp and implement the code in Python. Also, print the results for different noise values in the Gaussian case, mean =0, 5, 10, 20 and sigma = 0, 20, 50, 100 and for the salt-and-pepper case, pa = 0.01, 0.03, 0.05, 0.4 and pb = 0.01, 0.03, 0.05, 0.4.**

- Please check the respective Exercise 3 folder in the repository for code and results.

**2. Change the kernel sizes for all the filters with all different values for noises and print the results for 3x3, 5x5 and 7x7 kernels. Comment on the results. Which filter seems to work "better" for images with salt-and-pepper noise and gaussian noise?**

- Increasing the kernel size increased the blurriness of the images. Median filter works better for Salt and Pepper Noise while Gaussian filter works better for Gaussian Noise.

## Exercise 4

**1. Look at Threshold.cpp and implement the code in Python, and observe the results for dierent threshold values. Comment on the results.**

- The output shows the 'baboon.jpg' image with different thresholds applied to its grayscaled version. We can see that different thresholds either highlight or tone down certain features of the image. We also observe that Adaptive filtering has the closest resemblance to the original image.

**2. What are the disadvantages of binary threshold?**

- Binary threshold gives maximum intensity to a pixel if its value is higher than the threshold value, and gives the minimum intensity to all other values. This method of giving only the extreme (maximum or minimum) values to pixels results in loss of details. 

**3. When is Adaptive Threshold useful?**

- Where an image has different lighting conditions in different areas, we go for adaptive thresholding. In this, the algorithm calculates the threshold for small regions of the image. So, we get different thresholds for different regions of the same image and it gives us better results for images with varying illumination.

## Exercise 5

**2. Object detection vs. Tracking: After looking at OpenCV face detection, you know that it works in real time and you can easily detect the face in every frame. So, why do you need tracking in the the first place?**

- Object *detection* in videos involves verifying the presence of an object in image sequences and possibly locating it precisely for recognition. Object *tracking* is to monitor an object’s spatial and temporal changes during a video sequence, including its presence, position, size, shape, etc. These two processes are closely related because tracking usually starts with detecting objects, while detecting an object repeatedly in subsequent image sequence is often necessary to help and verify tracking.
- For example, if we consider the example of face detection, usual models are trained for frontal faces. If a face turns to the side, the face detector would fail to recognize it as a face, but a carefully constructed tracker should work. In other words, any change in the object's appearance can be captured by a tracker.
