# 1. Develop a program to display a grayscale image using read and write operation?<br>
pip install opencv-python<br>
import cv2<br>
img=cv2.imread('F1.jfif',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
![image](https://user-images.githubusercontent.com/97940151/174038089-0609c4b5-63a7-4835-ae9a-b3eebab4484b.png)<br>
<br>
<br>
<br>
# 2. Develop a program to display the image using matplotlib?<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('F1.jfif')<br>
plt.imshow(img)<br>
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
![image](https://user-images.githubusercontent.com/97940151/174041325-6755a879-4216-49e7-ae20-13a5c31b9320.png)
<br>
<br>
<br>
# 5.Write a program to create using a color?<br>
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,0,0))<br>
img.show()<br>
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
OUTPUT<br>
![image](https://user-images.githubusercontent.com/97940151/174045745-6264bf37-0373-48de-8677-0da4a745b40c.png)<br>



