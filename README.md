# EX-03 Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.

## Program:
```python
# Developed By: Manoj Kumar G
# Register Number: 212222230078

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.jpg")
color_image = cv2.imread("color.webp",-1)
gray_image = cv2.resize(gray_image,(300,400))
color_image = cv2.resize(color_image,(400,200))
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
Gray_image = cv2.imread("gray.jpg")
Color_image = cv2.imread("color.webp")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()

plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()

gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
<img src ="https://github.com/Adhithyaram29D/Histogram-of-an-images/assets/119393540/9a646993-0942-4f77-9f1b-268b7fddbc5a" width="300">
<br>
<img src ="https://github.com/Adhithyaram29D/Histogram-of-an-images/assets/119393540/3bde2cba-0755-452d-8b70-42fdfb7187ce" width="500">

### Histogram of Grayscale Image and any channel of Color Image
<img src= "https://github.com/Adhithyaram29D/Histogram-of-an-images/assets/119393540/924c724d-83e4-4d00-9908-ab6f17f6400b" height="300">
<img src ="https://github.com/Adhithyaram29D/Histogram-of-an-images/assets/119393540/b87e0022-d811-48e9-875d-041754adf4db" width="400">
<br>
<img src ="https://github.com/Adhithyaram29D/Histogram-of-an-images/assets/119393540/fbc7e642-34e7-4106-bcd3-f248ded98e92" width="300">
<img src= "https://github.com/Adhithyaram29D/Histogram-of-an-images/assets/119393540/1cd65408-e4fc-4ff9-ae5e-4e6ca0911b6c" width="400">

### Histogram Equalization of Grayscale Image.
<img src= "https://github.com/Adhithyaram29D/Histogram-of-an-images/assets/119393540/e5b8c4db-5131-40d0-9a13-2ffafde3fa1f" height="400">
<img src ="https://github.com/Adhithyaram29D/Histogram-of-an-images/assets/119393540/544b3058-63d4-4305-a4c0-1d62a9e0d22a" height="400">

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
