# EX-6 EDGE-DETECTION
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
```
DEVELOPED BY: PRAVEEN S
REGISTER NUMBER: 212222240078
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("eagle.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![eagle](https://github.com/Praveen0500/EDGE-DETECTION/assets/120218611/3abc4b63-d47c-4042-80e1-cd674e08d4a5)
### SOBEL EDGE DETECTOR:
![image](https://github.com/Praveen0500/EDGE-DETECTION/assets/120218611/b0960e12-2f53-47d3-8ac3-5a63fb0e9035)
![image](https://github.com/Praveen0500/EDGE-DETECTION/assets/120218611/4ca9c3a3-aedf-4278-a511-0a1e0b74eabb)
![image](https://github.com/Praveen0500/EDGE-DETECTION/assets/120218611/df6f44c6-9636-47e6-b843-9bfbf43fbcd3)
### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Praveen0500/EDGE-DETECTION/assets/120218611/fed31a30-1ae3-438f-ae13-ac9f2afe1148)
### CANNY EDGE DETECTOR
![image](https://github.com/Praveen0500/EDGE-DETECTION/assets/120218611/48a60036-d9e9-46c3-991e-0319bd5dada8)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
