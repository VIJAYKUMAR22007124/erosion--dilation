# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>
Import the necessary packages.

### Step2:
<br>
Create the Text using cv2.putText

### Step3:
<br>
Create the structuring element

### Step4:
<br>
Erode the image

### Step5:
<br>
Dilate the image

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'VIJAY',(80,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')

# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:



### Display the input Image
<br>
<br>
<img width="291" alt="{24E43306-AC61-4BC2-8EBE-4343A0B3D712}" src="https://github.com/user-attachments/assets/8f74f9a6-2a1c-42c5-b243-d7d21af8a708">

<br>
<br>

### Display the Eroded Image
<br>
<br>
<img width="290" alt="{C208435C-F9B0-4E54-B64F-14115DBB72BF}" src="https://github.com/user-attachments/assets/f4ad4868-e241-4da4-b6a5-8f3e245939c8">

<br>
<br>

### Display the Dilated Image
<br>
<br>
<img width="291" alt="{27227918-8AA1-4348-B5C7-7B02FB6CF007}" src="https://github.com/user-attachments/assets/a33abed2-5ed9-4dd7-86d4-4fd3b48b86e3">
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
