# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: S PAVITHRAN
# Register Number: 212223240113
```



### Input Grayscale Image and Color Image
```
import cv2
from matplotlib import pyplot as plt
#Load the color image
image = cv2.imread('image.png')
#Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
## Output:
<img width="350" height="520" alt="Screenshot 2025-09-06 083603" src="https://github.com/user-attachments/assets/81bd5c6e-4e27-407e-9916-5752b5b6dd02" />


### Histogram of Grayscale Image
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
## Output:
<img width="743" height="586" alt="Screenshot 2025-09-06 083613" src="https://github.com/user-attachments/assets/4bb7b97f-16c9-41de-ad15-ede23090d29f" />


### Histogram Equalization of Grayscale Image.
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```
## Output:

<img width="374" height="519" alt="Screenshot 2025-09-06 083620" src="https://github.com/user-attachments/assets/d521c8f2-765d-4034-abe2-e761b6f702b7" />

## Equalized Histogram
```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output:
<img width="753" height="546" alt="Screenshot 2025-09-06 083628" src="https://github.com/user-attachments/assets/b7350ece-0cd7-45be-989f-0e3653677158" />

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
