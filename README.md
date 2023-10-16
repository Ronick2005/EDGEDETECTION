# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.
### Step2:
Read the image and convert the bgr image to gray scale image.
### Step3:
Use any filters for smoothing the image to reduse the noise.
### Step4:
Apply the respective filters -Sobel, Laplacian edge detector and Canny edge detector.
### Step5:
Display the filtered image using plot and imshow.
 
## Program:
## Import the packages
``` python
import cv2
import matplotlib.pyplot as plt
```
## Load the image, Convert to grayscale and remove noise
``` python
img=cv2.imread("dipt.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

## SOBEL EDGE DETECTOR
### SOBEL X AXIS :
``` python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### SOBEL Y AXIS :
``` python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### SOBEL XY AXIS :
``` python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

## LAPLACIAN EDGE DETECTOR
``` python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```


## CANNY EDGE DETECTOR
``` python
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR
#### SOBEL X AXIS :
![image](https://github.com/Ronick2005/EDGEDETECTION/assets/83219341/17509e48-9874-4003-a998-a9562bbc3375)

#### SOBEL Y AXIS :
![image](https://github.com/Ronick2005/EDGEDETECTION/assets/83219341/a4b62daf-fef2-460e-ac77-f3f19aaf02c2)

#### SOBEL XY AXIS :
![image](https://github.com/Ronick2005/EDGEDETECTION/assets/83219341/3464ce9e-addf-40af-9a74-9d2a2314adac)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Ronick2005/EDGEDETECTION/assets/83219341/321e5670-b9de-4178-b9ed-b641e9c8d2c5)

### CANNY EDGE DETECTOR
![image](https://github.com/Ronick2005/EDGEDETECTION/assets/83219341/8ec32b13-8414-46df-9dd8-3eb65a0e8f2c)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
