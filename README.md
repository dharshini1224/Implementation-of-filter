# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
# Step1
Import the required libraries.

# Step2
Convert the image from BGR to RGB.

# Step3
Apply the required filters for the image separately.

# Step4
Plot the original and filtered image by using matplotlib.pyplot.

# Step5
End the program

## Program
### Developed By   :Dharshini.S
### Register Number:212224230061
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("billie.png")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()



```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()





```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()





```
iv)Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()






```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()






```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

<img width="910" height="767" alt="image" src="https://github.com/user-attachments/assets/d7d34628-6947-4f9a-a8f1-ac8043e2a6ce" />


ii)Using Weighted Averaging Filter

<img width="641" height="507" alt="image" src="https://github.com/user-attachments/assets/bccfc2d8-9808-456d-ba9b-b229ff31bc7c" />


iii)Using Gaussian Filter

<img width="636" height="510" alt="image" src="https://github.com/user-attachments/assets/0747420e-e704-406f-a6c8-de468b949d6b" />


iv) Using Median Filter

<img width="913" height="738" alt="image" src="https://github.com/user-attachments/assets/4b362361-8895-427f-9099-e6fc9eac8861" />


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

<img width="627" height="517" alt="image" src="https://github.com/user-attachments/assets/db56aa76-b536-4945-b211-7c6ca8a9ab5e" />

ii) Using Laplacian Operator

<img width="631" height="512" alt="image" src="https://github.com/user-attachments/assets/0c94649e-f074-4c6c-b7c1-65e4bc47cc0b" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
