# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By:Naveenaa A K
### Register Number: 212222230094


## Output:

### i)Read and Display an Image
```
import cv2
image=cv2.imread('panda.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/95ec792c-f40d-423e-ab71-2255ede1ba1f)

<br>
<br>

### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image.
```
import cv2
img = cv2.imread("panda.jpg")
res = cv2.line(img, (0, 0), (1099, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
![image](https://github.com/user-attachments/assets/eea784bb-eb94-4af8-a5eb-481dc62a2457)

ii)Draw a circle at the center of the image.
```
import cv2

# Load the image
img = cv2.imread("panda.jpg")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 150, (255, 0, 0), 10)

# Display the image with the circle
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/eb4d16ce-21a7-427e-9ac3-e99651a3283b)

iii)Draw a rectangle around a specific region of interest in the image.
```
import cv2

img = cv2.imread("panda.jpg")
start=(0,0)
stop=(318,200)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/a501d0f7-5d5c-4f27-8866-c3cb36314d1c)


iv)Add the text "PANDA" at the top-left corner of the image.
```
import cv2

# Load the image
img = cv2.imread("panda.JPG")

# Define the text to be added and its position
text = "OPENCV DRAWING"
position = (50, 50)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/user-attachments/assets/272ac12c-27f6-44ea-8ce7-7a988bec4584)

<br>
<br>

### iii)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/8c45ab3d-2ccd-4774-b6df-7c354ba24694)

ii.)Convert the image from RGB to GRAY and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/688e73a3-1f1d-41a3-a51c-0ab2992337bb)
iii.)Convert the image from RGB to YCrCb and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/3dced8f9-6777-4544-99c0-89a39e6d79a4)
iv.)Convert the HSV image back to RGB and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/user-attachments/assets/d409a35c-45fa-4192-9dfc-bc8570cf81d8)

<br>
<br>

### iv)Access and Manipulate Image Pixels
```
import cv2

# Load and resize the image
img = cv2.imread('panda.jpg', 1)
img = cv2.resize(img, (300, 200))

# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()

```
![image](https://github.com/user-attachments/assets/ec9e7025-cae2-4e84-9fa0-3ac3eb477cd9)

![image](https://github.com/user-attachments/assets/3daabe1e-4587-4218-a9fa-84e0920d4d82)

<br>
<br>

### v)Image Resizing
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/user-attachments/assets/2e0858d4-3a48-4bfe-834c-0bff33096473)

<br>
<br>

### vi)Image Cropping
```
import cv2

# Load the image
image1=cv2.imread('panda.jpg',1)

# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 100, 100

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/c5a2c209-d4f6-4fdf-b0bf-448f90365428)

<br>
<br>

### vii)Image Flipping
i.)Flip the original image horizontally and display it.
```
import cv2
img = cv2.imread("panda.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/06be2d2e-d9a0-4bc6-9b00-af47050b57dc)
ii.)Flip the original image vertically and display it.
```
import cv2

img = cv2.imread("panda.JPG")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/04e8d8d4-e476-47b6-b3fc-a8a807fef19c)

<br>
<br>

### viii)Write and Save the Modified Image
```
 cv2.imwrite('panda.jpg',image)
```
![image](https://github.com/user-attachments/assets/a2ab057a-430d-492a-be5b-988cc0ccde5d)

<br>
<br>






## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







