# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION
## Aim
To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

Image Erosion

Image Dilation

## Software Used
Anaconda – Python 3.7

Jupyter Notebook / VS Code

OpenCV (cv2)

NumPy

Matplotlib

## Algorithm
### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Create a blank image using NumPy.

### Step 3:
Insert text onto the image using OpenCV's text drawing function.

### Step 4:
Display the original image.

### Step 5:
Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion
Apply the erosion operation using the created kernel.

Remove pixels from the boundaries of foreground objects.

Display the eroded image.
### Step 7: Image Dilation
Apply the dilation operation using the same kernel.

Add pixels to the boundaries of foreground objects.

Display the dilated image.
### Step 8:
Compare the original, eroded, and dilated images.

### Program
#### Developed By
Name: T.GOSHANRAJAN

Register No: 212225040098
#### Step 1:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
#### Step 2:
```
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
#### Step 3:
```
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'This is T.GOSHANRAJAN', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
#### Step 4:
```
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
#### Output:
<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/46048d24-d9e3-439f-be01-0820e19e27e7" />


#### Step 5:
```
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
```
#### Step 6:
```
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```

#### Output:
<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/ce9317a8-b764-437d-992d-95320fff6236" />


#### Step 7:
```
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
### Output

<img width="389" height="410" alt="image" src="https://github.com/user-attachments/assets/b68e01b3-00c4-4777-b4d1-a44ea53928a9" />


### Result
Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV.
