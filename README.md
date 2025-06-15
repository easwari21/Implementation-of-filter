# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.
## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>
Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program
### Developed By   :AJINA JOSHPIN 
### Register Number:212223230008
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("/content/thala.png")
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
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```
median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
</br>

# i) Using Averaging Filter
![image](https://github.com/user-attachments/assets/9935fd4f-aa19-46f1-b243-296bd728ac78)

# ii)Using Weighted Averaging Filter
![image](https://github.com/user-attachments/assets/8806ab6d-c5e3-4dcd-ba1d-715c047639fd)


# iii)Using Gaussian Filter
![image](https://github.com/user-attachments/assets/e96b06bc-6571-4b2f-b24f-1946dac18554)


# iv) Using Median Filter
![image](https://github.com/user-attachments/assets/eefd7cfb-3d86-4a80-8819-9bb70b000a46)

### 2. Sharpening Filters


# i) Using Laplacian Kernal
![image](https://github.com/user-attachments/assets/bac3b6f1-6719-4be0-9949-25b351bfc482)


# ii) Using Laplacian Operator
![image](https://github.com/user-attachments/assets/dee8dff9-edb0-4a0b-bf8c-f86527145533)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
