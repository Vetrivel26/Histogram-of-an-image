# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.


## Program:
```python
# Developed By: SURYA R
# Register Number: 212220230052
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('nature.jpg')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()


# Display the histogram of gray scale image and any one channel histogram from color image
Color_image=cv2.imread('21.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 
Gray_image=cv2.imread('21.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image
![Screenshot (243)](https://user-images.githubusercontent.com/75236145/164978581-b392bf76-6094-4ef0-a32a-4b8bbeb7b20a.png)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot (243)1](https://user-images.githubusercontent.com/75236145/164978585-c5a447ed-7d92-4367-a784-fb1cd953020e.png)
![Screenshot (242)](https://user-images.githubusercontent.com/75236145/164978590-ec40bc61-9dce-4843-b197-83eddde104fd.png)


### Histogram Equalization of Grayscale Image
![Screenshot (244)](https://user-images.githubusercontent.com/75236145/164978823-61d9f86c-0e8e-4c6f-a914-f81f50ce97fd.png)
![Screenshot (245)](https://user-images.githubusercontent.com/75236145/164978828-4206e880-f6aa-466b-ab9a-fc6570d8950d.png)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
