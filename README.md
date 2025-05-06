# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages
<br>

### Step2:

Create the Text using cv2.putText
<br>

### Step3:
Create the structuring element
<br>

### Step4:
Use Opening operation
<br>

### Step5:
Use Closing Operation
<br>

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
#i) Create the Text using cv2.putText
img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"YUVARAM S",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()
#ii) Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
#iii) Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()
#iv) Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

### Display the input Image
<br>
<br>
<br>
<br>


![Screenshot 2025-05-06 160954](https://github.com/user-attachments/assets/4229bc99-e5b0-469e-a63f-982bef40acca)

<br>
<br>

### Display the result of Opening
<br>
<br>
<br>
<br>

![Screenshot 2025-05-06 161003](https://github.com/user-attachments/assets/0201ad02-bdd2-4575-bc99-afc81f9f3bed)

<br>
<br>

### Display the result of Closing
<br>
<br>

<br>![Screenshot 2025-05-06 161012](https://github.com/user-attachments/assets/517bab4a-f036-497f-b947-9d9a6e1ac006)

<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
