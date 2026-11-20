# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION

## Name: Renick Fabian Rajesh
## Reg No: 212224230227


## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

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

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Renick Fabian Rajesh', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

```

<img width="595" height="801" alt="image" src="https://github.com/user-attachments/assets/228ef87e-a66d-4145-ac76-8d87d6ff8de6" />

```

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

```

<img width="515" height="411" alt="image" src="https://github.com/user-attachments/assets/99fe4620-1524-411c-9d6d-efae94dace81" />

```

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

```

<img width="522" height="416" alt="image" src="https://github.com/user-attachments/assets/aea87eba-d885-4e4e-8103-036b54586d47" />

```

# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```

<img width="527" height="427" alt="image" src="https://github.com/user-attachments/assets/c2786145-a003-4a3c-98e4-e74788e399d0" />




## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
