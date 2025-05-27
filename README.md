# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:
Import the necessary packages.
#### Step2:
Create the Text using cv2.putText
#### Step3:
Create the structuring element
#### Step4:
Erode the image
#### Step5:
Dilate the image

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline

def load_img():
    blank_img =np.zeros((500,500))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img,text='SAI',org=(50,300), fontFace=font,fontScale= 5,color=(255,255,255),thickness=25,lineType=cv2.LINE_AA)
    return blank_img

def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()


# Erode the image
kernel = np.ones((5,5),dtype=np.uint8)
erosion1 = cv2.erode(img, kernel,iterations=1)
display_img(erosion1)


# Dilate the image
kernel1 = np.ones((7,7),dtype=np.uint8)
dilation = cv2.dilate(img,kernel1,iterations=1)
display_img(dilation)



```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/f10ca6d0-93db-428e-8f32-957db5d8064e)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/77540caf-65cb-4911-aee0-9c5aea481a9d)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/0715961b-dbf9-400e-bb4a-963cfb5b39ae)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
