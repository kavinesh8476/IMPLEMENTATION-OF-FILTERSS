# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.
</br> 

### Step2
Convert the image from BGR to RGB.
</br> 

### Step3
Apply the required filters for the image separately.
</br> 

### Step4
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
End the program.
</br> 

## Program:
### Developed By   : Kavinesh M
### Register Number: 212222230064
</br>

### 1. Smoothing Filters
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("a.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
### i) Using Averaging Filter
```Python
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
### ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
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
### iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
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

### iv) Using Median Filter
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
### i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
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
### ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
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

### i) Using Averaging Filter
![image](https://github.com/kavinesh8476/IMPLEMENTATION-OF-FILTERSS/assets/118466561/ea5ca55d-18a6-4df3-b2c0-bbc4f54218fd)
</br>

### ii) Using Weighted Averaging Filter
![image](https://github.com/kavinesh8476/IMPLEMENTATION-OF-FILTERSS/assets/118466561/cecf91fe-e9f9-46b4-8afb-1bc8ec02a2b2)
</br>

### iii) Using Gaussian Filter
![image](https://github.com/kavinesh8476/IMPLEMENTATION-OF-FILTERSS/assets/118466561/87f9ae14-2b4d-49c1-b665-2dd671b0e111)

</br>

### iv) Using Median Filter
![image](https://github.com/kavinesh8476/IMPLEMENTATION-OF-FILTERSS/assets/118466561/e56cb8f2-3ebe-4408-a273-20703b1b1559)
</br>

### 2. Sharpening Filters
</br>

### i) Using Laplacian Kernal
![image](https://github.com/kavinesh8476/IMPLEMENTATION-OF-FILTERSS/assets/118466561/f27bee94-aa2a-43d9-8c51-09ec857594d5)

</br>

### ii) Using Laplacian Operator
![image](https://github.com/kavinesh8476/IMPLEMENTATION-OF-FILTERSS/assets/118466561/ab632530-b184-449c-ad49-835684671656)

</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
