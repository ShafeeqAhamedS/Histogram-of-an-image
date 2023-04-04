# <p align="center">Histogram and Histogram Equalization of an image</p>

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
### Step4:
cv2.equalize() is used to transform the gray image to equalized form.
### Step5:
The Histogram of gray scale image and color image is shown.

## Program:
Developed By: **Shafeeq Ahamed. S**
</br>

Register Number: **212221230092**


### a) Write your code to find the histogram of gray scale image and color image channels.

```python
import cv2
import matplotlib.pyplot as plt

# Gray Scale Image
im = cv2.imread("mikasa_c.png",0)
cv2.imshow("Mikasa",im)

hist = cv2.calcHist([im],[0],None,[256],[0,255])

# Colour Image
im_c = cv2.imread("mikasa_c.png",1)
cv2.imshow("Mikasa",im_c)

hist_c = cv2.calcHist([im_c],[1],None,[256],[0,255])
```

### b) Display the histogram of gray scale image and any one channel histogram from color image

```py
plt.figure()
plt.title("Histogram of B/W Image")
plt.xlabel("GrayScale Values")
plt.ylabel("Pixel Count")
plt.stem(hist)
plt.show()

plt.figure()
plt.title("Histogram of B/W Image")
plt.xlabel("GrayScale Values")
plt.ylabel("Pixel Count")
plt.stem(hist_c)
plt.show()
```

### c) Write the code to perform histogram equalization of the image. 
```py
equ = cv2.equalizeHist(im)
cv2.imshow("Mikasa",equ)
hist1 = cv2.calcHist([equ],[0],None,[256],[0,255])
plt.figure()
plt.title("Histogram of B/W Image")
plt.xlabel("GrayScale Values")
plt.ylabel("Pixel Count")
plt.stem(hist1)
plt.show()
```
## Output:
### Input Grayscale Image and Color Image
<p align="center">
<img width="350" src="https://user-images.githubusercontent.com/93427237/229816886-4f272f87-463a-4378-90bc-d1bfca63a02d.png">
<img width="350" src="https://user-images.githubusercontent.com/93427237/229817353-622c401d-63dc-4a4c-b069-0482b2d5afa4.png">
</p>

### Histogram of Grayscale Image and any channel of Color Image
<p align="center">
<img width = "375" src="https://user-images.githubusercontent.com/93427237/229817011-290c1bb4-9ed9-40e6-aa87-acb1ab0c3aae.png">
<img width = "375" src="https://user-images.githubusercontent.com/93427237/229817481-e4ecc37c-59ba-41d9-92c1-542052166cdb.png">
</p>

### Histogram Equalization of Grayscale Image

<p align="center">
<img width="400" src="https://user-images.githubusercontent.com/93427237/229817147-b6f81b76-adfb-4321-99c3-7b075f13e923.png">
<img width="450" src="https://user-images.githubusercontent.com/93427237/229817236-655526de-26e7-4d83-90c8-9eab1f0c5982.png">
</p>
                                                                                                                            

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
