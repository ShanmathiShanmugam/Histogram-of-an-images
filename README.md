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
# Developed By: S.Shanmathi
# Register Number: 212222100049

import cv2
import matplotlib.pyplot as plt
image= cv2.imread("ajith.jpeg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.subplot(1, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(gray_image, cmap='gray')
plt.title('Grayscale Image')
plt.axis('off')

hist= cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Gray Scale Value')
plt.ylabel('Pixel Count')
plt.stem(range(256), hist)
plt.show()

equ = cv2.equalizeHist(gray_image)
plt.imshow(equ,cmap='gray')
plt.title('Equalized Image')
plt.show()

equ_hist = cv2.calcHist([equ], [0], None, [256], [0, 256])
plt.figure()
plt.title("Equalized Histogram")
plt.xlabel('Gray Scale Value')
plt.ylabel('Pixel Count')
plt.stem(range(256), equ_hist)
plt.show()

image1 = cv2.imread('vijay.jpeg')
gray_image1=cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)

plt.subplot(2,1,1)
plt.imshow(cv2.cvtColor(image1,cv2.COLOR_BGR2RGB))
plt.title('Original image')
plt.axis('off')

plt.subplot(2,1,2)
plt.imshow(gray_image1,cmap='gray')
plt.title('Grayscale Image')
plt.axis('off')
plt.show()

hist1 = cv2.calcHist([gray_image1], [0], None, [256], [0, 256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Gray Scale Value')
plt.ylabel('Pixel Count')
plt.stem(range(256), hist1)
plt.show()

equ1 = cv2.equalizeHist(gray_image1)
plt.imshow(equ1, cmap='gray')
plt.title('Equalized Image')
plt.show()

equ_hist1 = cv2.calcHist([equ], [0], None, [256], [0, 256])
plt.figure()
plt.title("Equalized Histogram")
plt.xlabel('Gray Scale Value')
plt.ylabel('Pixel Count')
plt.stem(range(256), equ_hist1)
plt.show()
```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/ShanmathiShanmugam/Histogram-of-an-images/assets/121243595/9715131b-33b9-4eff-ad8d-a88f8db84732)

![image](https://github.com/ShanmathiShanmugam/Histogram-of-an-images/assets/121243595/59d2f561-2c32-447a-9e9a-fdf03f6537dc)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/ShanmathiShanmugam/Histogram-of-an-images/assets/121243595/a1f321f5-c744-4e52-9dc8-f5fe2e17fb34)

![image](https://github.com/ShanmathiShanmugam/Histogram-of-an-images/assets/121243595/cd4d4a87-8a8f-4642-bc5c-69e376a5ce71)

### Histogram Equalization of Grayscale Image.

![image](https://github.com/ShanmathiShanmugam/Histogram-of-an-images/assets/121243595/42caa93e-1b87-4049-8aa7-737497023255)

![image](https://github.com/ShanmathiShanmugam/Histogram-of-an-images/assets/121243595/378826bb-f1af-42f7-acf7-121623d0e5bd)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
