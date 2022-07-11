# 1. Develop a program to display a grayscale image using read and write operation?<br>
pip install opencv-python<br>
import cv2<br>
img=cv2.imread('F1.jfif',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
<br>
OUTPUT:-<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174038089-0609c4b5-63a7-4835-ae9a-b3eebab4484b.png)<br>
<br>
<br>
<br>
# 2. Develop a program to display the image using matplotlib?<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('F1.jfif')<br>
plt.imshow(img)<br>
<br>
OUTPUT:-<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174039132-01d337a3-80c1-4204-bfd9-cb5a1514dab7.png)<br>
<br>
<br>
<br>
# 3. Develop a program to perform a linear transformation using rotation?<br>
import cv2<br>
from PIL import Image<br>
img=Image.open('F1.jfif')<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
<br>
OUTPUT:-<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174040352-3f9bea71-216a-4061-815f-cab7a428f5d5.png)<br>
<br>
<br>
<br>
# 4. Develop a program to convert color tree to RCB color values?<br>
from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>                           
img3=ImageColor.getrgb("pink")<br>
print(img3)<br>
<br>
OUTPUT:-<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174041325-6755a879-4216-49e7-ae20-13a5c31b9320.png)
<br>
<br>
<br>
# 5.Write a program to create using a color?<br>
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,0,0))<br>
img.show()<br>
<br>
OUTPUT:-<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174042123-12f038b4-ff4f-4e51-8af6-d2f0690fccb3.png)<br>
<br>
<br>
<br>
# 6. Develop a program to visualize the image using various color spaces?<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=cv2.imread('F1.jfif')<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
plt.imshow(img)<br>
plt.show()<br>
<br>
OUTPUT:-<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174044873-31e49b84-bced-4a2f-b705-9ec5a36332e1.png)<br>
![image](https://user-images.githubusercontent.com/97940151/174048463-920d342c-a558-4a75-b35d-22bc46358095.png)<br>
<br>
<br>
<br>
# 7. Develop a program to display the image attributes?<br>
from PIL import Image<br>
image=Image.open('F1.jfif')<br>
print("Filename:",image.filename)<br>
print("Format:",image.format)<br>
print("Mode:",image.mode)<br>
print("Size:",image.size)<br>
print("Width:",image.width)<br>
print("Height:",image.height)<br>
image.close()<br>
<br>
OUTPUT:-<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174045745-6264bf37-0373-48de-8677-0da4a745b40c.png)<br>
<br>
<br>
<br>
# 8. Convert the original image to gray scale and then to binary?<br>
import cv2<br>
img=cv2.imread('F1.jfif')<br>
cv2.imshow("RGB",img)<br>
cv2.waitKey(0)<br>
img=cv2.imread('F1.jfif',0)<br>
cv2.imshow("Gray",img)<br>
cv2.waitKey(0)<br>
ret,bw_img=cv2.threshold(img,127,255,cv2.THRESH_BINARY)<br>
cv2.imshow("Binary",bw_img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
<br>
OUTPUT:-<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174049483-f5d7ce12-36b2-44df-8596-8a1ed25cafe7.png)<br>
![image](https://user-images.githubusercontent.com/97940151/174049629-845c7b1a-c884-4987-aaa6-6d83dbf7b8b6.png)<br>
![image](https://user-images.githubusercontent.com/97940151/174049816-3e6b0c76-03ba-4a7f-86ed-e9cb35c1c89c.png)<br>
<br>
<br>
<br>
# 9. Resize the original image?<br>
import cv2<br>
img=cv2.imread('F1.jfif')<br>
print('original image length width',img.shape)<br>
cv2.imshow('original image',img)<br>
cv2.waitKey(0)<br>
imgresize=cv2.resize(img,(150,160))<br>
cv2.imshow('Resized image',imgresize)<br>
print('Resized image length width',imgresize.shape)<br>
cv2.waitKey(0)<br>
<br>
OUTPUT:-<br>
original image length width (181, 278, 3) Resized image length width (160, 150, 3) -1<br>
![image](https://user-images.githubusercontent.com/97940151/178219499-b7d4ba70-830a-4d33-bb4a-25f78e0e9b1e.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178219546-85693bc0-2448-4c6a-a2c5-7ed1868b1a50.png)
<br>
<br>
<br>

 10. Develop a program to read image using URL ?<br>
 url from skimage import io<br>
 import matplotlib.pyplot as plt<br>
 url='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ3VyCF39_x0MhTZema9w9qnFPw6SgAAnY0lA&usqp=CAU'<br>
 image=io.imread(url)<br>
 plt.imshow(image)<br>
 plt.show()<br>
 OUTPUT:-<br>
![image](https://user-images.githubusercontent.com/97940151/178225320-9bd09b8c-73a2-4b6e-8e93-744847b3d237.png)

11. Write a program to mask and blur the image?<br>
import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>
img=cv2.imread('img5.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
![image](https://user-images.githubusercontent.com/97940151/175018482-7fbc79fa-0e2f-476f-b161-a5f88d921047.png)<br>

hsv_img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
light_orange=(1,190,200)<br>
dark_orange=(18,255,255)<br>
mask=cv2.inRange(img,light_orange,dark_orange)<br>
result=cv2.bitwise_and(img,img,mask=mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result)<br>
plt.show()<br>
<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/175019101-a8f8672f-89d2-4c6d-afce-d3185ca09c65.png)<br>

light_white=(0,0,200)<br>
dark_white=(145,60,255)<br>
mask_white=cv2.inRange(hsv_img,light_white,dark_white)<br>
result_white=cv2.bitwise_and(img,img,mask=mask_white)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask_white,cmap='gray')<br>
plt.subplot(1,2,2)<br>
plt.imshow(result_white)<br>
plt.show()<br>
<br>

![image](https://user-images.githubusercontent.com/97940151/175021934-41f82d64-17da-4c0b-9fc6-e985d177198c.png)<br>
