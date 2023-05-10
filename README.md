# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

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
Use Opening and Closing Operations

### Step5:
End Program.

 
## Program:
```
DEVELOPED BY: M.Suwetha
REG NO: 212221230112
```
``` 
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((500,800),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Thalapathy vijay",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
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

![i-1](https://github.com/swemurali/Opening-and-Closing/assets/94165336/8c29ac12-37dd-4a77-867d-bb79ae3ec135)

### Display the result of Opening

![i-2](https://github.com/swemurali/Opening-and-Closing/assets/94165336/d390720f-bbe4-4d9d-8c55-b3ba5429b919)

### Display the result of Closing

![i-3](https://github.com/swemurali/Opening-and-Closing/assets/94165336/d53caa8c-0162-4484-b9f8-14a637e59f9c)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
