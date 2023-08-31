# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import opencv
<br>

### Step2:
Read the original Image.
<br>

### Step3:
Store the required conversion of the image in a variable.
<br>

### Step4:
Show the image stored in the given variable.
<br>

### Step5:
Destroy all the windows and end the program.
<br>

## Program:
### Developed By: T.S.Yamunaasri
### Register Number:212222240117
### i) Convert BGR and RGB to HSV and GRAY
```
import cv2
houseImage = cv2.imread('pic.jpeg')
cv2.imshow('Original Image',houseImage)
hsvImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(houseImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(houseImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### ii)Convert HSV to RGB and BGR
```
import cv2
houseHSVImage = cv2.imread('pic.jpeg')
cv2.imshow('Original HSV Image',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### iii)Convert RGB and BGR to YCrCb
```
import cv2
houseImage = cv2.imread('pic.jpeg')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### iv)Split and Merge RGB Image
```
import cv2
image = cv2.imread('pic.jpeg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged BGR image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### v) Split and merge HSV Image
```
import cv2
image = cv2.imread('pic.jpeg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow
```




## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot 2023-08-31 222241](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/fac7825c-7e53-4e91-8339-23afd1aeb5b7)

![Screenshot 2023-08-31 222254](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/37f9d47b-2288-47d9-b019-9172f119842f)

![Screenshot 2023-08-31 222305](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/10523f0c-4a24-4bbc-9883-e0a618f1c783)

![Screenshot 2023-08-31 222316](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/89b4026f-a01b-4cee-a5bd-8342dad2e09d)

![Screenshot 2023-08-31 222326](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/a614e5db-384f-4076-9e44-c61b4ee4b2a6)

<br>
<br>

### ii) HSV to RGB and BGR

![Screenshot 2023-08-31 223209](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/3c15d82b-9246-40d9-8222-ef2be7622f86)

![Screenshot 2023-08-31 223219](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/044fd045-2e66-42f7-8947-f6c55d29ecea)

![Screenshot 2023-08-31 223232](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/47c4adea-68a4-43eb-8416-666e3281456b)

<br>
<br>

### iii) RGB and BGR to YCrCb
![Screenshot 2023-08-31 223209](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/b3e792e3-dede-4b9f-9e23-0f46f48e0bc2)


![Screenshot 2023-08-31 223840](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/8a6b5301-7f65-48d3-8a9b-5d2cfc1fddf4)


![Screenshot 2023-08-31 223850](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/957b3893-5393-41d5-98b4-fb792b705a66)

<br>
<br>

### iv) Split and merge RGB Image
![Screenshot 2023-08-31 224046](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/4c66f5dd-fd1d-460c-830b-fc12febbe9e4)

![Screenshot 2023-08-31 224100](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/a828f477-bdd1-435a-b2bd-37469798915c)

![Screenshot 2023-08-31 224109](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/88e83cc3-1e65-4779-8307-1fc6ef1d1229)

![Screenshot 2023-08-31 224121](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/273aa11f-2365-4205-a7c3-19af58309887)

<br>
<br>

### v) Split and merge HSV Image

![Screenshot 2023-08-31 224353](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/50eccce3-9396-45cb-9dd3-ecf28fe84a24)

![Screenshot 2023-08-31 224404](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/1b90bdcc-c3a3-47f2-86f2-b66e0d3b6f0f)

![Screenshot 2023-08-31 224415](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/481486cc-fcf8-430f-aa8d-97e2b6222f6a)

![Screenshot 2023-08-31 224430](https://github.com/Yamunaasri/COLOR-CONVERSION/assets/115707860/648ae816-2dbc-4f61-98d5-b4f7a81c2a33)

<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
