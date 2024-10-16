# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:

Load the necessary packages.

### Step2:

Read the Image and convert to grayscale.

### Step3:

Use Global thresholding to segment the image.

### Step4:

Use Adaptive thresholding to segment the image.

### Step5:

Use Otsu's method to segment the image and display the results.

## Program
```
Developed by:Giftson Rajarathinam N
Register number:212222233002

```
```python
# Load the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read the Image and convert to grayscale

image = cv2.imread('HappyFish.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(gray_image, cmap='gray')
plt.title('Grayscale Image')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Global thresholding to segment the image

ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Adaptive thresholding to segment the image

th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY, 11, 2)

# Display the adaptive thresholding result
plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()




# Use Otsu's method to segment the image 
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)



# Display the results
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()




```
## Output:

### Original Image:
![decaprio](https://github.com/user-attachments/assets/dc244323-3003-4b8a-aac8-af4438328493)
### Greyscale Image:
![Screenshot 2024-10-16 142342](https://github.com/user-attachments/assets/d715950b-8277-4d8d-a27a-f4c5e987b3bf)

### Global Thresholding:
![Screenshot 2024-10-16 142411](https://github.com/user-attachments/assets/ebe517d7-eecc-4be2-94ca-031f5a81321d)


### Adaptive Thresholding:
![Screenshot 2024-10-16 142450](https://github.com/user-attachments/assets/9500ad9b-d7f4-4b9d-a16d-51a97e154e42)


### Optimum Global Thesholding using Otsu's Method:
![Screenshot 2024-10-16 142518](https://github.com/user-attachments/assets/663cae71-b477-45c4-a568-8495ed73920d)



## Result:
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
