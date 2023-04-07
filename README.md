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
Reflect of image.
### Step 6:
Rotate the image & Crop the image.
### Step 7:
Display all the Transformed images.

## Program:
Developed By: Senthil Kumar S
Register Number: 212221230091

### Original Image
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

```py
rows,cols,dim=img.shape
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
<img width="600" src="https://user-images.githubusercontent.com/93427237/230407148-56296213-b9cf-4a7b-8812-8e7d8edb17a4.png">

### i)Image Translation
<img width="600" src="https://user-images.githubusercontent.com/93427237/230405553-bdbf48f9-2914-4a2d-ae8e-4691ad7a0401.png">

### ii) Image Scaling
<img width="600" src="https://user-images.githubusercontent.com/93427237/230405581-d744e036-06d4-437a-8177-e348ae1f217c.png">

### iii)Image shearing
<img width="600" src="https://user-images.githubusercontent.com/93427237/230405598-5537f03b-f9a8-43c8-b367-eb51b3ca1875.png">

### iv)Image Reflection
<img width="600" src="https://user-images.githubusercontent.com/93427237/230406107-741bb81d-dae6-4784-a99c-da12e2ae8765.png">
<img width="600" src="https://user-images.githubusercontent.com/93427237/230406086-405f6ffe-6b75-4c50-be77-43b38a9bf346.png">

### v)Image Rotation
<img width="600" src="https://user-images.githubusercontent.com/93427237/230405730-26b893d6-80e4-4162-9f6d-7695d5470593.png">

### vi)Image Cropping
<img width="600" src="https://user-images.githubusercontent.com/93427237/230405762-ab9abe3e-d33d-43b0-8626-3a89fadac87d.png">

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
