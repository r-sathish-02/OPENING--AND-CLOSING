## OPENING--AND-CLOSING
### Aim
To implement Opening and Closing using Python and OpenCV.

### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:
Import the necessary packages
#### Step2:
Create the Text using cv2.putText
#### Step3:
Create the structuring element
#### Step4:
Use Opening operation
#### Step5:
Use Closing Operation

### Program:
```
Developed by: Sathish R
Register Number:212222230138
```
#### Display the input Image
```
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'CELANZA', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
#### Create ths structured element
```
struct_ele = np.ones((9, 9), np.uint8)
```
#### Display the result of Opening
```
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
#### Display the result of Closing
```
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
### Output:

#### Display the input Image
![dip_ex_10_1](https://github.com/r-sathish-02/OPENING--AND-CLOSING/assets/118787261/b0bdd51d-cdf9-438b-9216-9541c9b11ab6)


#### Display the result of Opening
![dip_ex_10_2](https://github.com/r-sathish-02/OPENING--AND-CLOSING/assets/118787261/c40308cb-3e31-4c54-8fb6-997ca0172de4)


#### Display the result of Closing
![dip_ex_10_3](https://github.com/r-sathish-02/OPENING--AND-CLOSING/assets/118787261/5129acc6-06e7-4aef-afb0-57337b02511c)


### Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
