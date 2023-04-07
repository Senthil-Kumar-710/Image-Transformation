# <p align="center">Image-Transformation</p>
## AIM:
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step 2:
Translate the image.
### Step 3:
Scale the image.
### Step 4:
Shear the image.
### Step 5:
Reflect the image.
### Step 6:
Rotate the image & Crop the image.
### Step 7:
Display all the Transformed images.

## Program:
Developed By: Senthil Kumar S
<br>
Register Number: 212221230091

### Original Image
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("jotaro.jpg")
img = cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
cv2.imshow("Image",img)
cv2.waitKey(0)
cv2.destroyAllWindows()
plt.axis('off')
plt.imshow(img)
plt.show()
```
```py
rows,cols,dim=img.shape
```

### i)Image Translation
```py
M=np.float32([[1,0,200],
             [0,1,250],
             [0,0,1]])
translated_img=cv2.warpPerspective(img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()
```

### ii) Image Scaling
```py
M=np.float32([[1.5,0,0],
             [0,1.5,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```


### iii)Image shearing
```py
M_x=np.float32([[1,0.2,0],
               [0.2,1,0],
               [0,0,1]])
sheared_img = cv2.warpPerspective(img,M_x,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img)
plt.show()
```

### iv)Image Reflection
```py
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_yaxis=cv2.warpPerspective(img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```
### v)Image Rotation
```py
angle1=np.radians(5)
angle2=np.radians(35)
angle3=np.radians(5)
angle4=np.radians(45)
M=np.float32([[np.cos(angle1),-(np.sin(angle2)),0],
               [np.sin(angle3),np.cos(angle4),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
### vi)Image Cropping
```py
cropped_img=img[150:1500,1000:3000]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### Original Image
![im1](https://user-images.githubusercontent.com/93860256/230664704-60680692-6751-4810-8b2e-36ef4aff9d61.png)

### i)Image Translation
![im2](https://user-images.githubusercontent.com/93860256/230665041-4bbc389d-3411-498d-91ba-dfe56309e14a.png)

### ii) Image Scaling
![im3](https://user-images.githubusercontent.com/93860256/230665042-33d3e619-57d2-4ea7-be31-1d895bc97269.png)

### iii)Image shearing
![im4](https://user-images.githubusercontent.com/93860256/230665023-5e5edb55-4495-4c3c-aa5e-8da948c0d162.png)

### iv)Image Reflection
![im5](https://user-images.githubusercontent.com/93860256/230665029-54a00fb3-ca07-49bf-886d-93a6a00f8577.png)
<br>
![im6](https://user-images.githubusercontent.com/93860256/230665032-8810d67f-4e77-4a6b-a0b5-4e6c51278ea7.png)

### v)Image Rotation
![im7](https://user-images.githubusercontent.com/93860256/230665035-48488781-df23-4cb3-ba2f-9d0dd228f1fc.png)

### vi)Image Cropping
![im8](https://user-images.githubusercontent.com/93860256/230665038-1fd92f0a-783f-4602-92f9-7b1f71a84907.png)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
