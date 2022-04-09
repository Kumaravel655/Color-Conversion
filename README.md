# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

Import cv2 and save and image as filename.jpg
### Step2:

Use imread(filename, flags) to read the file.

### Step3:

Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:

Split and merge the image using cv2.split and cv2.merge commands.

### Step5:

End the program and close the output image windows.

## Program:
```python
# Developed By: KUMARAVEL V
# Register Number: 212220230027
```
### i) Convert BGR and RGB to HSV and GRAY
```python
import cv2
color_image = cv2.imread('ee.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```


### ii)Convert HSV to RGB and BGR


```python
import cv2
color_image = cv2.imread('ee.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

```
### iii)Convert RGB and BGR to YCrCb

```python
import cv2
color_image = cv2.imread('ee.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

```
### iv)Split and Merge RGB Image
```python
import cv2
image = cv2.imread('ee.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

```
### v) Split and merge HSV Image
```python
import cv2
image = cv2.imread('ee.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot (56)](https://user-images.githubusercontent.com/75235334/162568992-951f21fa-5d48-4750-8f98-e2c02d8db1dc.png)


### ii) HSV to RGB and BGR

![Screenshot (57)](https://user-images.githubusercontent.com/75235334/162569036-70d7dc59-e978-4697-b6df-08fa128cb706.png)
### iii) RGB and BGR to YCrCb

![Screenshot (58)](https://user-images.githubusercontent.com/75235334/162569068-7972af2b-101c-4275-83a9-1c94b475a3d1.png)

### iv) Split and merge RGB Image
![Screenshot (60)](https://user-images.githubusercontent.com/75235334/162569193-a42d8bb7-f4a0-4d0c-bc6c-bd195d4ba3a0.png)


### v) Split and merge HSV Image

![Screenshot (59)](https://user-images.githubusercontent.com/75235334/162569165-30dec521-7f9d-4bf7-a5a6-df1e5abe7564.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
