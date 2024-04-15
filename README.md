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
```
 Developed By: ARUN KUMAR SUKDEV CHAVAN
 Register Number: 212222230013
```
### Input Grayscale Image and Color Image

```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("thala.jpg")
color_image = cv2.imread("thalapathy.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Yogeshvar005/Histogram-of-an-images/assets/113497367/155119b1-9150-4cf3-a8f0-1ea6581d0870)

![image](https://github.com/Yogeshvar005/Histogram-of-an-images/assets/113497367/7f3b7dde-9adf-406a-a9d0-638af267cb01)

### Histogram of Grayscale Image and any channel of Color Image

```python
import numpy as np
Gray_image = cv2.imread("thala.jpg")
Color_image = cv2.imread("thalapathy.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
#### Grayscale Image

![image](https://github.com/Yogeshvar005/Histogram-of-an-images/assets/113497367/0ae42ed3-faae-4eaa-b40b-ac2d3af82613)

![image](https://github.com/Yogeshvar005/Histogram-of-an-images/assets/113497367/2b6c4a83-190e-4d5a-9def-bd610f550714)

#### Color Image

```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
![image](https://github.com/Yogeshvar005/Histogram-of-an-images/assets/113497367/c2884609-3cbf-47b0-9fef-ee27ee03232d)
![image](https://github.com/Yogeshvar005/Histogram-of-an-images/assets/113497367/f0a9a86e-1eba-4e8e-ae95-d23e7b90b286)


### Histogram Equalization of Grayscale Image.

```python
import cv2
gray_image = cv2.imread("thala.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Yogeshvar005/Histogram-of-an-images/assets/113497367/fcd0bae7-9708-488b-8504-56310d781d11)

![image](https://github.com/Yogeshvar005/Histogram-of-an-images/assets/113497367/3f4fbae7-e244-49e6-ab03-8d4d3a99f234)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
