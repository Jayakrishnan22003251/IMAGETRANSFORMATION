# IMAGE TRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.
<br>

### Step2:
Write a code to translation of the image.
<br>

### Step3:
Write a code for scaling of the image.
<br>

### Step4:
Write a code for shearing of the image.
<br>

### Step5:
Write a code for reflection of the image.
<br>

### Step6:
Write a code to rotation of the image.

### Step7:
Write a code to cropping of the image.

### Step8:
Display all the Transformed images.


## Program:

##### Developed By: JAYAKRISHNAN L B L
##### Register Number:  212222230052

i)Image Translation:

```
import numpy as np
import matplotlib.pyplot as plt 
import cv2 as cv

image = cv.imread("color.jpg")
image = cv.cvtColor(image, cv.COLOR_BGR2RGB)

plt.axis("off")
plt.imshow(image)
plt.show()

#translation of an image :

rows,cols,dim = image.shape

M = np.float32([[1,0,100], [0,1,50],[0,0,1]])
translated_image= cv.warpPerspective(image, M, (cols, rows))

plt.axis("off")
plt.imshow(translated_image)
plt.show()
```


ii) Image Scaling:
```
rows,cols,dim = image.shape

M_scale = np.float32([[1,0,0], [0,1.5,0],[0,0,1]])
scale_image= cv.warpPerspective(image, M_scale, (cols, rows))

plt.axis("off")
plt.imshow(scale_image)
plt.show()

```


iii)Image shearing:
```
M_x = np.float32([[1,1,0], [0,1,0],[0,0,1]])

M_y = np.float32([[1,0,0], [0.4,1,0],[0,0,1]])

shear_imagex= cv.warpPerspective(image, M_x, (cols, rows))
shear_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(shear_imagex)
plt.show()

plt.axis("off")
plt.imshow(shear_imagey)
plt.show()
```



iv)Image Reflection:
```
M_x = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

M_y = np.float32([[-1,0,cols], [0,1,0],[0,0,1]])

ref_imagex= cv.warpPerspective(image, M_x, (cols, rows))
ref_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(ref_imagex)
plt.show()

plt.axis("off")
plt.imshow(ref_imagey)
plt.show()

```



v)Image Rotation:
```
angle = 90 
height, width = image.shape[:2]
rotation_matrix = cv.getRotationMatrix2D((width / 2, height / 2), angle, 1)
rotated_image = cv.warpAffine(image, rotation_matrix, (width, height))
plt.figure(figsize=(10, 5))
plt.subplot(1, 2, 1)
plt.title('Original Image')
plt.imshow(cv.cvtColor(image, cv.COLOR_BGR2RGB))
plt.subplot(1, 2, 2)
plt.title('Rotated Image')
plt.imshow(cv.cvtColor(rotated_image, cv.COLOR_BGR2RGB))

plt.show()

```



vi)Image Cropping:
```
x1, y1 = 100, 100 
x2, y2 = 300, 300 
cropped_image = image[y1:y2, x1:x2]
plt.subplot(1, 2, 1)
plt.title('Cropped Image')
plt.imshow(cv2.cvtColor(cropped_image, cv.COLOR_BGR2RGB))
plt.show()

```
## Output:
### i)Image Translation:
![image](https://github.com/Jayakrishnan22003251/IMAGETRANSFORMATION/assets/120232371/e6659997-ae78-4ad1-9439-cefe7657034e)


![image](https://github.com/Jayakrishnan22003251/IMAGETRANSFORMATION/assets/120232371/8df1cef8-7f69-403e-917a-c90e9f694cbf)







### ii) Image Scaling:
![image](https://github.com/Jayakrishnan22003251/IMAGETRANSFORMATION/assets/120232371/e7d46b82-bfa1-47fd-beec-79ad274007a9)



### iii)Image shearing:
![image](https://github.com/Jayakrishnan22003251/IMAGETRANSFORMATION/assets/120232371/93b4e97e-181e-44b7-b927-31204735ee7e)
![image](https://github.com/Jayakrishnan22003251/IMAGETRANSFORMATION/assets/120232371/47d098e3-4b3d-44c2-a145-c371ed92af63)



### iv)Image Reflection:
![image](https://github.com/Jayakrishnan22003251/IMAGETRANSFORMATION/assets/120232371/1228af8e-9b8a-4afe-8a6b-0a5080a64e48)


![image](https://github.com/Jayakrishnan22003251/IMAGETRANSFORMATION/assets/120232371/00e995cd-78f0-44e2-91af-833adc6feb71)


### v)Image Rotation:
![image](https://github.com/Jayakrishnan22003251/IMAGETRANSFORMATION/assets/120232371/7ef3d135-1142-4647-8bad-0ed6a5bfbd1e)




### vi)Image Cropping:

![image](https://github.com/Jayakrishnan22003251/IMAGETRANSFORMATION/assets/120232371/e4679aca-c120-4a53-ad09-a5e43c3d9745)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
