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


