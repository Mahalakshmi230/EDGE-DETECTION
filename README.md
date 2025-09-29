# EDGE-DETECTION
# Developed By:Daniel C
# Reg no:212223240023
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
# Developed By: Mahalakshmi R
# Reg no:212223230116
# Program:
```

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('cat.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

# SOBEL EDGE DETECTOR
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')

# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:
# Original image:
<img width="572" height="563" alt="image" src="https://github.com/user-attachments/assets/bdcf0f52-cd3c-499c-ac7b-a37d0dc6d4d8" />

### SOBEL EDGE DETECTOR
<img width="566" height="572" alt="image" src="https://github.com/user-attachments/assets/26af9145-ef58-449d-b956-36e7d8fa89b0" />


### LAPLACIAN EDGE DETECTOR
<img width="561" height="558" alt="image" src="https://github.com/user-attachments/assets/d7b7641d-47e2-4080-a3d7-5b6d27960a43" />


### CANNY EDGE DETECTOR
<img width="567" height="570" alt="image" src="https://github.com/user-attachments/assets/f4e9a73b-45b6-4d0e-a476-f2a2e010195b" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
