# OPENING--AND-CLOSING
## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

 
## Program:

 Python
Name: Naveen Kumar V
Ref no: 212223230140
``` 
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
# Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Amruthavarshini', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
# Create a simple square kernel (3x3)
```
kernel = np.ones((3, 3), np.uint8)
```
# Display the input image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
# Opening is erosion followed by dilation
```
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
```
# Display the result of Opening
```
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```
# Closing is dilation followed by erosion
```
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(closed_image)
plt.axis("off")
```

## Output:




### Display the result of Opening
<br>
<br>
<br>
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/af0afa15-9dcc-4f7b-ac2a-c7b60eb76fb8" />




<br>
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/271c08cc-c802-483c-b418-91be08c55910" />




<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
