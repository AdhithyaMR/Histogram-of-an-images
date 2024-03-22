# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: ADHITHYA M R
# Register Number: 212222240002
```
# Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("dala_na.png")
color_image = cv2.imread("smillepathi.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Histogram of Grayscale image and color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("dala_na.png")
Color_image = cv2.imread("smillepathi.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
# Histogram equalization of Grayscale image
```
import cv2
gray_image = cv2.imread("smillepathi.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image

![Screenshot 2024-03-22 092856](https://github.com/AdhithyaMR/Histogram-of-an-images/assets/118834761/72122c3d-e57b-46ef-889d-c5111258b339)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-22 093115](https://github.com/AdhithyaMR/Histogram-of-an-images/assets/118834761/1a2959cd-9760-4ad7-8f06-939a06fa056a)

![Screenshot 2024-03-22 093141](https://github.com/AdhithyaMR/Histogram-of-an-images/assets/118834761/31cd54cd-294b-4b8b-9afd-abe5b2008d85)


### Histogram Equalization of Grayscale Image.


![Screenshot 2024-03-22 093234](https://github.com/AdhithyaMR/Histogram-of-an-images/assets/118834761/407efbbb-2159-4261-81b3-51a05d5c67c8)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
