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

Developed By: JEEVAGOWTHAM S
Register Number:  212222230053

i)Image Translation:

```
import numpy as np
import matplotlib.pyplot as plt 
import cv2 as cv
```
```
#plotting of an image :

image = cv.imread("tree.jpg")
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
rotation_matrix = cv2.getRotationMatrix2D((width / 2, height / 2), angle, 1)
rotated_image = cv2.warpAffine(image, rotation_matrix, (width, height))
plt.figure(figsize=(10, 5))
plt.subplot(1, 2, 1)
plt.title('Original Image')
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.subplot(1, 2, 2)
plt.title('Rotated Image')
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB))

plt.show()

```



vi)Image Cropping:
```
x1, y1 = 100, 100 
x2, y2 = 300, 300 
cropped_image = image[y1:y2, x1:x2]
plt.subplot(1, 2, 2)
plt.title('Cropped Image')
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB))

plt.show()







```
## Output:
### i)Image Translation:
![Screenshot 2023-09-08 141339](https://github.com/JeevaGowtham-S/IMAGETRANSFORMATION/assets/118042624/3695f48b-c3b1-4b9b-bfa8-fd6e25764055)

![Screenshot 2023-09-08 194235](https://github.com/JeevaGowtham-S/IMAGETRANSFORMATION/assets/118042624/449db3bd-ec0d-4040-aaa2-5e215228fe18)

<br>
<br>
<br>
<br>

### ii) Image Scaling:
![Screenshot 2023-09-08 194253](https://github.com/JeevaGowtham-S/IMAGETRANSFORMATION/assets/118042624/c170acaa-a696-4647-8531-e09efc21d762)

<br>
<br>
<br>
<br>


### iii)Image shearing:
![Screenshot 2023-09-08 142317](https://github.com/JeevaGowtham-S/IMAGETRANSFORMATION/assets/118042624/d9e454ce-8402-4cbc-be23-e2935d483369)
![Screenshot 2023-09-08 142327](https://github.com/JeevaGowtham-S/IMAGETRANSFORMATION/assets/118042624/43f6ec3a-b5e7-4292-a6d9-99c5691ecc40)



<br>
<br>
<br>
<br>


### iv)Image Reflection:
![Screenshot 2023-09-08 141339](https://github.com/JeevaGowtham-S/IMAGETRANSFORMATION/assets/118042624/851212e9-5a96-43f0-97be-550c9cc13b86)
![Screenshot 2023-09-08 142608](https://github.com/JeevaGowtham-S/IMAGETRANSFORMATION/assets/118042624/6d521577-9378-4ea7-9f68-9685e15492f3)

<br>
<br>
<br>
<br>



### v)Image Rotation:
![Screenshot 2023-09-08 195814](https://github.com/JeevaGowtham-S/IMAGETRANSFORMATION/assets/118042624/647c2bc5-7675-4b09-9143-a110bcf4fc1a)




<br>
<br>
<br>
<br>



### vi)Image Cropping:

![Screenshot 2023-09-08 200126](https://github.com/JeevaGowtham-S/IMAGETRANSFORMATION/assets/118042624/f8a4d147-e1de-4f05-8aa9-e74f62c7986f)


<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
