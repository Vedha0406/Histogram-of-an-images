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


## PROGRAM:
```
# Developed By:VEDHASHREE.G
# Register Number:212223240171

!pip install opencv-python

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('gray_image.jpeg')
color_image = cv2.imread('color_image.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
gray_image=cv2.imread('gray_image.jpeg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

import numpy as np
color_image=cv2.imread('color_image.jpg')
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

import cv2
gray_image = cv2.imread("gray_image.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![370150998-1d75cf71-cb44-47e0-b206-3b825f80d149](https://github.com/user-attachments/assets/6a1dadea-1c64-4a6a-b693-c9ad5e6dfcd4)
![370151055-c56c02ad-30c7-450f-a192-1867c1c18f2a](https://github.com/user-attachments/assets/d3349c9a-67f9-4e05-96bb-6fb14917b4b7)
### Histogram of Grayscale Image and any channel of Color Image
![370151208-e4f7c0f9-a2fc-4245-b60f-0ab6d51b737c](https://github.com/user-attachments/assets/f9ab21ab-6812-4252-98d0-7cc2c52200ba)
![370151208-e4f7c0f9-a2fc-4245-b60f-0ab6d51b737c](https://github.com/user-attachments/assets/a02237e0-9892-4ada-bd28-abd9076ee48e)
![370151410-7ae17351-df74-4212-9d53-24e04aff2fb8](https://github.com/user-attachments/assets/18045b7d-3ec7-442f-bb8d-e1d89fe3f937)
### Histogram Equalization of Grayscale Image
![370151525-2339f1d9-57fc-4acd-ab07-1810f7d508f0](https://github.com/user-attachments/assets/3792f712-6320-421f-8e53-fc55d33b08aa)
![370151660-b030a54b-562e-4cd3-9738-f7af0f2fa46a](https://github.com/user-attachments/assets/3e2b1d28-4774-4f06-8b90-b71d1bad121e)
## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
