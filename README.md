# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM:
Developed by : SRIRAM S S

Reg.no : 212222230150

```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("tiger.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/2eb7e358-5b6f-45e9-ba21-327c977607f9)

### SOBEL EDGE DETECTOR
#### SOBEL X AXIS
```python
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
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/dd50e39d-7fee-4ae1-9e55-5f18e8e0e220)
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/2835dc43-b41a-4d12-a87a-ee1db2f282f9)


#### SOBEL Y AXIS
```python
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
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/8b209b2d-171e-41c8-a5ba-acd66339abff)
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/7080d87a-aea2-4d78-89d3-bc71ea5c615b)


#### SOBEL XY AXIS
```python
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
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/e8dda3cd-568e-4c54-8198-28166968459a)
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/6075e655-6d96-433e-b299-cf2286397382)


### LAPLACIAN EDGE DETECTOR
```python
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
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/8f962b07-4ec3-495a-9dfd-e248ac31e44c)      
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/3838b839-4e50-43d0-a62f-8cb07293d624)


### CANNY EDGE DETECTOR
```python
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
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/cc4cbd22-12e9-489c-890a-3d6d8acd11b4)            
![image](https://github.com/Yogeshvar005/EDGE-DETECTION/assets/113497367/fe39386e-4653-43bc-9d60-3935230fd952)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
