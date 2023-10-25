# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

Step1: Import the necessary packages.

Step2: Create the text image using cv2.putText.

Step3: Then create the structuring image for dilation/erosion.

Step4: Apply erosion and dilation using plt.erode and plt.dilate.

Step5: Plot the images using plt.imshow.

 
## Program:

```
Developed By: G Lutheesh
Reg No.: 212221230029
```
```
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText

image = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"Jayanth",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()

# Create the structuring element

kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Erode the image

image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()


# Dilate the image

image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()






```
## Output:

### Display the input Image
![WhatsApp Image 2023-10-25 at 11 13 44_24e57de2](https://github.com/Lutheeshgoparapu/EROSION-AND-DILATION/assets/94154531/a013d120-19ee-40bb-8ae3-f76a2fc19415)


### Display the Eroded Image
![WhatsApp Image 2023-10-25 at 11 13 54_a1a76f9d](https://github.com/Lutheeshgoparapu/EROSION-AND-DILATION/assets/94154531/3a21d0fb-ca1b-4eb8-bd19-ba956f55923a)


### Display the Dilated Image
![WhatsApp Image 2023-10-25 at 11 14 08_b4699458](https://github.com/Lutheeshgoparapu/EROSION-AND-DILATION/assets/94154531/aebd8869-fe98-4641-87ce-d3aa8eb8f41d)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
