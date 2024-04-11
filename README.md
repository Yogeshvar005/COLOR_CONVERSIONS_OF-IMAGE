# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

## Program:
#### Developed By: Yogeshvar.M
#### Register Number: 212222230180


## Output:

### i) Read and display the image

```python
     import cv2
    image=cv2.imread('pass.jpg',1)
    image=cv2.resize(image,(300,300))
    cv2.imshow('Yogi',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows() 

```
![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/3d1cf8eb-8206-4e84-94ed-d8abc8c07554)

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/29a97cf3-5116-400b-a772-9a23aebe2549)

### ii)Write the image

```python
   image=cv2.imread('pass.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/7599ed25-96a7-4092-9071-b3061a564cd8)

### iii)Shape of the Image

```python
    image=cv2.imread('pass.jpg',1)
    print(image.shape)
```
![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/688c1870-69fe-4f41-b57e-0e8b3a8e6464)

### iv)Access rows and columns

```python
import random
    image=cv2.imread('pass.jpg',1)
    image=cv2.resize(image,(500,500))
    for i in range (250,500):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/dd0ae5b6-86c1-48c8-854f-007e35a4fb53)

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/510ae999-f782-4610-b071-5ff8394d5c88)


### v)Cut and paste portion of image

```python
    image=cv2.imread('pass.jpg',1)
    image=cv2.resize(image,(300,300))
    tag =image[150:200,110:160]
    image[110:160,150:200] = tag
    cv2.imshow('image1',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/daf8f1bd-b24d-45b3-935e-199c757d3a3a)

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/8724c02f-ee89-409e-a405-9000227c3c73)

### vi) BGR and RGB to HSV and GRAY

```python
    img = cv2.imread('pass.jpg',1)
    img = cv2.resize(img,(200,200))
    cv2.imshow('Original Image',img)

    hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
    cv2.imshow('BGR2HSV',hsv1)

    hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
    cv2.imshow('RGB2HSV',hsv2)
    
    gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
    cv2.imshow('BGR2GRAY',gray1)
    
    gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
    cv2.imshow('RGB2GRAY',gray2)
    
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/a4f0d771-3292-48d4-adfd-e28aa5774a48)

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/75ecf890-a3ac-4b45-a559-c0c7c81af2bb)


### vii) HSV to RGB and BGR

```python
img = cv2.imread('pass.jpg')
img = cv2.resize(img,(200,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/6ab89956-2220-4c39-9b00-6652f121e04a)

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/0bcd17b4-3794-4153-9c39-25bb6d251f3c)


### viii) RGB and BGR to YCrCb

```python
img = cv2.imread('pass.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/7e02f573-250b-417e-89d3-24a8dbc8d05e)

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/56a06dab-07ce-4188-a89d-4babfeecaf8a)


### ix) Split and merge RGB Image
```python
img = cv2.imread('pass.jpg',1)
img = cv2.resize(img,(200,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/9b67b1d9-33a3-4e93-aed9-6ccb7dbbe656)

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/f0f19574-d0af-4c66-a490-dbe7d833d2af)

### x) Split and merge HSV Image
```python
img = cv2.imread("pass.jpg",1)
img = cv2.resize(img,(200,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/38520ae8-c43b-4faa-9bf7-db303eb1fe8d)

![image](https://github.com/Yogeshvar005/COLOR_CONVERSIONS_OF-IMAGE/assets/113497367/fdfba9d4-2406-4910-b416-f0644513413f)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







