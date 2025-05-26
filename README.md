# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:
```
#NAME:Dakshata G
#REG NO:212223240021
import cv2
import numpy as np
import matplotlib.pyplot as plt

img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Dakshata",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image

![Screenshot 2025-05-26 170138](https://github.com/user-attachments/assets/87ea4eb3-74b7-457b-9d4c-633482b11d11)



### Display the result of Opening

![Screenshot 2025-05-26 170145](https://github.com/user-attachments/assets/dca59133-0a94-4a56-844c-fe24ffbcc318)




### Display the result of Closing

![Screenshot 2025-05-26 170151](https://github.com/user-attachments/assets/73e2e64f-ea76-4fbb-a430-eb89c7fe93cf)





## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
