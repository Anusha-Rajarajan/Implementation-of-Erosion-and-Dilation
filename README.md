# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:

Create the Text using cv2.putText.

### Step3:

Create the structuring element.

### Step4:

Erode and Dilate the image.

### Step5:

End the Program.

## Program:

Developed by : Anusha R

Register number :212221230006

``` Python

# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1 = np.zeros((100,230), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'anusha',(5,70), font, 2,(255),5,cv2.LINE_AA)
plt.imshow(img1,'gray')

# Create the structuring element

kernel=np.ones((5,5),np.uint8)
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
image_erode1=cv2.erode(img1, kernel)
plt.imshow(image_erode1, 'gray')

# Erode the image

image_erode1=cv2.erode(img1, kernel)
plt.imshow(image_erode1, 'gray')

# Dilate the image

image_dilate1 = cv2.dilate(img1, kernel)
plt.imshow(image_dilate1, 'gray')


```
## Output:

### Display the input Image

![10a](https://user-images.githubusercontent.com/93427472/235294670-35ef9e28-25c2-4bd3-a9e6-0a8daebc06d9.png)

### Display the Eroded Image

![10b](https://user-images.githubusercontent.com/93427472/235294681-4a93af6b-c066-4c51-a744-3618b1b2d81f.png)

### Display the Dilated Image

![10c](https://user-images.githubusercontent.com/93427472/235294709-6099cfa0-f737-405c-9252-859da66e5c89.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
