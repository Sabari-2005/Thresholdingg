# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm
### Step1:
Translation moves the image along the x or y-axis.

### Step2:
Scaling resizes the image by scaling factors.

### Step3:
Shearing distorts the image along one axis.

### Step4:
Reflection flips the image horizontally or vertically.

### Step5:
Rotation rotates the image by a given angle.


## Program
### Name:Sabarinath.R
### Register Number: 212223100048
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('ts.jpeg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')
plt.show()

_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
plt.show()

plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
plt.show()

plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
plt.show()
```
## Output
### Original Image
![Screenshot 2025-04-30 132601](https://github.com/user-attachments/assets/dd892867-2cc5-487c-9143-08f6e2bbb3ef)

### Global Thresholding
![Screenshot 2025-04-30 132608](https://github.com/user-attachments/assets/0215a8d3-33da-449f-a840-51f119723563)


### Adaptive Thresholding
![Screenshot 2025-04-30 132616](https://github.com/user-attachments/assets/84cbee5e-ab1e-469d-a728-01207eb1ff4a)


### Optimum Global Thesholding using Otsu's Method
![Screenshot 2025-04-30 132635](https://github.com/user-attachments/assets/e7f49ece-7bac-4143-b6de-b7dfcf8cd594)


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
