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
# Developed By: VIKASH S
# Register Number: 212222240115



import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('photo.jpg')

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

# Plotting the original grayscale image, equalized image, and histograms
plt.figure(figsize=(10, 7))

# Show original grayscale image
plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original DARK Grayscale Image')
plt.axis('off')

# Show equalized grayscale image
plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

# Plot histogram of the original grayscale image
plt.subplot(2, 2, 3)
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

# Plot histogram of the equalized image
plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()



```
## Output:
### Input bright Grayscale Image and dark Image
![image](https://github.com/user-attachments/assets/5f3f4a01-ac11-40fe-b01e-60c1fda4d15a)    ![image](https://github.com/user-attachments/assets/a4d3d0d8-2778-49c9-a8cd-c9db783fbb11)



### original Histogram of bright Grayscale Image and Dark Image
#### Bright:
![image](https://github.com/user-attachments/assets/98d57190-4658-40fc-8339-fb08758ceb56)
#### Dark:
![image](https://github.com/user-attachments/assets/044606f0-74b9-497b-b5d7-236a8c38157a)

### Histogram Equalization of Grayscale Image.
#### Bright:
![image](https://github.com/user-attachments/assets/ebb61889-e85b-4a71-81b4-769892d63d00)

![image](https://github.com/user-attachments/assets/16ac4c0b-7c45-43e0-a08d-0d8366e57797)
#### Dark:
![image](https://github.com/user-attachments/assets/b436f0cb-c134-41aa-ad52-0f44e49c80f2)

![image](https://github.com/user-attachments/assets/b5428097-d76e-4155-857b-e87a3ab86fe2)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
