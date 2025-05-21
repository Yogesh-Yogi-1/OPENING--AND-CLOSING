# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries.
<br>


### Step2:
Create white noise image and use it to display the opening image.
<br>

### Step3:
Display the opening image.
<br>

### Step4:
Create black noise image and use it to display the closing image.
<br>
 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"YOGESH",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element

kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation

img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation

img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

### Display the input Image
![Screenshot 2025-05-21 102830](https://github.com/user-attachments/assets/9ba1e036-cd86-48ed-a1ba-88f05bb80424)

<br>
<br>

### Display the result of Opening
![Screenshot 2025-05-21 102926](https://github.com/user-attachments/assets/9bc4fc0a-c060-48ac-9a62-96554424f06b)

<br>
<br>

### Display the result of Closing
![Screenshot 2025-05-21 102956](https://github.com/user-attachments/assets/2566b5ae-ac59-4925-8093-06fcf1d440c5)

<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
