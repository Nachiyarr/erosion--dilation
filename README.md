# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
```
NAME: ALAGU NACHIYAR K
REG.NO: 212222240006
```
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'VASUNDRA',(5,60),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
cv2.erode(img,kernel)
```
# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
## Output:

### Display the input Image
![image](https://github.com/Nachiyarr/erosion--dilation/assets/113497340/2f9f9232-0b6c-40ee-bee7-cc11e36579e9)

### Display the Eroded Image
![image](https://github.com/Nachiyarr/erosion--dilation/assets/113497340/bca16ec0-9737-47ce-9644-9c00251e3eb8)

### Display the Dilated Image
![image](https://github.com/Nachiyarr/erosion--dilation/assets/113497340/d0af660c-a566-4201-b051-e863b5005001)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
