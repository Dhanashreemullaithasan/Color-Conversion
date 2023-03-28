# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 library and upload the image or capture an image.

### Step2:
Read the saved image using cv2.imread("filename.jpg").

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v])

### Step5:
Output the image using cv2.imshow("OUTPUT", image)

## Program:

Developed By:DHANASHREE M

Register Number:212221230018

## i) Convert BGR and RGB to HSV and GRAY
```
import cv2
house_color_image = cv2.imread('house.jpg')
cv2.imshow('original image',house_color_image)
hsv_image = cv2.cvtColor(house_color_image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
hsv_image1 = cv2.cvtColor(house_color_image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
gray_image = cv2.cvtColor(house_color_image,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
gray_image1 = cv2.cvtColor(house_color_image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## ii)Convert HSV to RGB and BGR
```
import cv2
img = cv2.imread("images.jfif")
img1= cv2.resize(img, (450,400))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
hsv_rgb = cv2.cvtColor(hsv, cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB", hsv_rgb)
hsv_bgr = cv2.cvtColor(hsv, cv2.COLOR_HSV2BGR)
cv2.imshow("HSV_BGR", hsv_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## iii)Convert RGB and BGR to YCrCb
```
import cv2
img = cv2.imread("img.jpg")
img1= cv2.resize(img, (450,300))
cv2.imshow("BGR_COLOR ", img1)
img_ycrcb = cv2.cvtColor(img1 , cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR_YCRCB ", img_ycrcb)
img_bgr = cv2.cvtColor(img1, cv2.COLOR_BGR2RGB)
cv2.imshow("RGB COLOR", img_bgr)
img_bgr_y = cv2.cvtColor(img_bgr, cv2.COLOR_BGR2YCrCb)
cv2.imshow("RGB2YCrCb", img_bgr_y)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## iv)Split and Merge RGB Image
```
import cv2
img = cv2.imread("i.jpg")
img1= cv2.resize(img, (450,390))
cv2
b,g,r = cv2.split(img1)
cv2.imshow("RED MODEL", r)
cv2.imshow("GREEN MODEL", g)
cv2.imshow("BLUE MODEL ", b)
merger = cv2.merge([b,g,r])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## v) Split and merge HSV Image
```
import cv2
img = cv2.imread("children.jfif")
img1= cv2.resize(img, (450,300))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
h,s,v = cv2.split(hsv)
cv2.imshow("RED MODEL", h)
cv2.imshow("GREEN MODEL", s)
cv2.imshow("BLUE MODEL ", v)
merger = cv2.merge([h,s,v])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### i) BGR and RGB to HSV and GRAY
![dipex31](https://user-images.githubusercontent.com/94165415/228332594-70ac164c-59cb-4525-8e3c-549dafe32a90.png)

### ii) HSV to RGB and BGR
![dipex32](https://user-images.githubusercontent.com/94165415/228332646-8fda8c57-be92-4b89-b249-0cf19c0df4b6.png)


### iii) RGB and BGR to YCrCb
![dipex33](https://user-images.githubusercontent.com/94165415/228333318-a0456d9c-8ca6-4915-b156-ce59e1d327b0.png)


### iv) Split and merge RGB Image
![dipex3](https://user-images.githubusercontent.com/94165415/228333402-fba20587-deb2-44d7-a555-97a07e72fe11.png)

### v) Split and merge HSV Image
![dipex35](https://user-images.githubusercontent.com/94165415/228333474-e2b8382d-0c50-4b6e-90a2-ecddffde7a0e.png)
![dipex351](https://user-images.githubusercontent.com/94165415/228333515-8089fa42-75a3-4b3b-94f9-6eeb877bdec2.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
