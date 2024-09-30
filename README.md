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

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('bi.jpg')

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [255], [0, 255])
# Plot histogram of the original grayscale image
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])


# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

# Plot histogram of the equalized image
hist_equalized = cv2.calcHist([equalized_image], [0], None, [255], [0, 255])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 255])
```
## Output:
### Input Grayscale Image and Color Image
![WhatsApp Image 2024-09-30 at 16 03 59_3a725e4e](https://github.com/user-attachments/assets/a822e2bb-33e0-4bf2-9ead-efdc396151aa)

### Histogram of Grayscale Image and any channel of Color Image

![WhatsApp Image 2024-09-30 at 16 04 22_6243cf20](https://github.com/user-attachments/assets/27ac508a-c2d6-4bb3-9d77-ee3934d6e49e)

### Histogram Equalization of Grayscale Image
![WhatsApp Image 2024-09-30 at 16 04 46_8fe76432](https://github.com/user-attachments/assets/044f798c-2f29-40dd-87d0-e5aaf624f7de)

### Histogram of the equalized image
![WhatsApp Image 2024-09-30 at 16 05 17_06ca00e0](https://github.com/user-attachments/assets/8f56e607-36b0-4d68-9962-97dc3534c44f)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
