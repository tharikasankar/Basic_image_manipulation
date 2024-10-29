# Basic_image_manipulation
## Developd by: THARIKA S
## Reg.No:212222230159
## Program:
```p
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('Apollo.jpg')
height=720
width=1280
print(f"Width: {width}, Height: {height}")
plt.figure(figsize=(10, 10))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
cv2.imwrite('Apollo-11-Launch.png', image)

```
![image](https://github.com/user-attachments/assets/42f3037f-964e-4026-9541-23713e6b1e55)
```p
img = cv2.imread('newzealand.jpg', cv2.IMREAD_COLOR)
print(img.shape)
plt.figure(figsize=[3, 3])
plt.imshow(img[:, :, ::-1])
plt.title("Original Image")
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/e35d8f44-794c-4ae0-abd4-8a04d2bd5885)
```p
x, y, a, b = 125, 125, 250, 250
cropped_img = img[y:y+b, x:x+a]
resized_img = cv2.resize(cropped_img,None, fx=2, fy=2)
flipped_img = cv2.flip(resized_img, 1)
plt.figure(figsize=[5, 5])
plt.imshow(flipped_img[:, :, ::-1])
plt.title("Cropped, Resized, and Flipped Image")
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/2e1a10d0-1f26-4efb-a6f3-ef40bceba123)
```p
img = cv2.imread('emerald.jpg')

gray_image = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
print("Grayscale Image Shape:", gray_image.shape)
plt.figure(figsize=(10, 10))
plt.imshow(gray_image)
plt.axis('on')
plt.title("Grayscale Image")
plt.show()
```
![image](https://github.com/user-attachments/assets/8f3661ac-4da4-4bec-b83e-502ca00482ab)
```p
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('apollo.jpg')
text = 'Apollo 11 Saturn V Launch, July 16, 1969'
position = (50, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)
thickness = 2
cv2.putText(img, text, position, font, font_scale, color, thickness)
start = (450, 69)      
stop = (700, 650)      
rect_color = (255, 0, 255)
rect_thickness = 10
cv2.rectangle(img, start, stop, rect_color, rect_thickness)
plt.figure(figsize=[12, 12])

plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/61f7cbc3-b4f2-4af7-8f92-59ead662cec0)
```p
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('newzealand.jpg')
text = 'Newzealand boat'
position = (50, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)
thickness = 2
cv2.putText(img, text, position, font, font_scale, color, thickness)
start = (330, 200)      
stop = (420, 320)      
rect_color = (255, 0, 255)
rect_thickness = 10
cv2.rectangle(img, start, stop, rect_color, rect_thickness)
plt.figure(figsize=[12, 12])
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/25c0fe6e-4e7d-4833-bf9d-dbf18e288e7d)
