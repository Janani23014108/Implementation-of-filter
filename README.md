# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2

Convert the image from BGR to RGB.

### Step3

Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5

End the program.

## Program:
### Developed By   : J.JANANI
### Register Number: 212223230085
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("ocean.png")
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
```
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
```
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
```
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
```
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
```
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


i) Using Averaging Filter

![436151602-6cad12a6-527f-463b-be11-e5ab4b72e7e2](https://github.com/user-attachments/assets/f02789dd-741d-450c-95d3-5c803fd7f334)


ii)Using Weighted Averaging Filter

![436151763-15bc9436-d7dd-44d2-be66-b592bdef4bf9](https://github.com/user-attachments/assets/894c945f-d460-491b-8df8-2c604522bfd5)


iii)Using Gaussian Filter

![436151828-b59d6ae4-9dcb-4491-9641-8327a697c18f](https://github.com/user-attachments/assets/5fb47f0d-56d0-4da4-af69-24bc877f14dc)


iv) Using Median Filter

![436151961-e9ab0061-f456-4182-ae7d-71c7b23ae939](https://github.com/user-attachments/assets/84927696-1118-413d-9b72-ec9255c971c6)


### 2. Sharpening Filters


i) Using Laplacian Kernal

![436152226-46d8263e-f0a5-4534-8ddb-27927dc6bbac](https://github.com/user-attachments/assets/562b414a-ed79-4aaa-a69b-8b11b1c491f7)


ii) Using Laplacian Operator

![436152376-517ea45e-582b-4c57-8da1-358e02bed62f](https://github.com/user-attachments/assets/7a8acf9e-d877-4616-8ed7-1191138c50a3)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
