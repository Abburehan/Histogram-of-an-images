# Histogram-of-an-images
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
# Developed By: SYED ABBU REHAN
# Register Number: 212223240165
```
```
## Gray Image And Color Image
import cv2
gray_img = cv2.imread('grayimage.jpg')
gray_img = cv2.resize(gray_img,(300,200))
color_img = cv2.imread('colorimage.jpg')
color_img = cv2.resize(color_img,(300,200))
cv2.imshow("Gray Image",gray_img)
cv2.imshow("Colour Image",color_img)
cv2.waitKey(0)
```
```
## Histogram of Grayscale Image
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('grayimage.jpg')
color_img = cv2.imread('colorimage.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```
```
## Histogram of Color Image
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('grayimage.jpg')
color_img = cv2.imread('colorimage.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(color_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
```
## Histogram Equilization of GrayScale Image
import cv2
gray_img = cv2.imread('grayimage.jpg',0)
gray_img = cv2.resize(gray_img,(300,200))
cv2.imshow('Grey Scale Image',gray_img)
equ = cv2.equalizeHist(gray_img)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
```
## Output:
### Input Grayscale Image and Color Image
![dip ex03 1 1](https://github.com/Abburehan/Histogram-of-an-images/assets/138849336/d9e56a66-5ee1-4f04-805c-04b38dd1c51e)
### Histogram of Grayscale Image
![dip ex03 1 2](https://github.com/Abburehan/Histogram-of-an-images/assets/138849336/e735b7d9-0e36-4def-8dde-64b627ccb1f5)
### Histogram of Color Image
![dip ex03 1 3](https://github.com/Abburehan/Histogram-of-an-images/assets/138849336/8d7279a3-8510-4705-8331-6cac23096f9f)
### Histogram Equalization of Grayscale Image.
![dip ex03 1 4](https://github.com/Abburehan/Histogram-of-an-images/assets/138849336/f67a46a7-92f3-4bdb-b453-d1f78e55f9b8)
## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
