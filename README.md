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
Give the input text using cv2.putText()

### Step3: 
Perform opening operation and display the result

### Step4 
Similarly, perform closing operation and display the result
 
## Program:
### Developed By : Hari Prasath. P
### Reg No : 212223230070

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Dentist',(5,70), font,2,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

# Use Opening operation
```
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```


# Use Closing Operation
```
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image

![Screenshot 2024-05-09 080757](https://github.com/Hari-Prasath-P-08/OPENING--AND-CLOSING/assets/139455593/40ecead9-a81f-497a-b9c4-cc14062bd051)

### Display the result of Opening

![Screenshot 2024-05-09 080757](https://github.com/Hari-Prasath-P-08/OPENING--AND-CLOSING/assets/139455593/60104603-b8cb-443b-b0e2-3cb713fd2152)

### Display the result of Closing

![Screenshot 2024-05-09 080803](https://github.com/Hari-Prasath-P-08/OPENING--AND-CLOSING/assets/139455593/afa487fc-eba6-4082-b77c-f4af351f5446)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
