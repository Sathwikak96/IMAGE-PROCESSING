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

 # 10. Develop a program to read image using URL ?<br>
 url from skimage import io<br>
 import matplotlib.pyplot as plt<br>
 url='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ3VyCF39_x0MhTZema9w9qnFPw6SgAAnY0lA&usqp=CAU'<br>
 image=io.imread(url)<br>
 plt.imshow(image)<br>
 plt.show()<br>
 OUTPUT:-<br>
![image](https://user-images.githubusercontent.com/97940151/178225320-9bd09b8c-73a2-4b6e-8e93-744847b3d237.png)

# 11. Write a program to mask and blur the image?<br>
import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>
img=cv2.imread('fish.jpg')<br><br>
plt.imshow(img)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940851/175256088-534b41d1-7204-4e74-8ffa-b2e07fd3a6a3.png)

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
![image](https://user-images.githubusercontent.com/97940851/175256433-cd6a66bd-0eec-42ed-9281-3a002ad19731.png)


light_white=(0,0,200)<br>
dark_white=(145,60,255)<br>
mask_white=cv2.inRange(hsv_img,light_white,dark_white)<br>
result_white=cv2.bitwise_and(img,img,mask=mask_white)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask_white,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result_white)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940851/175256779-ede4be6e-d028-445b-8ec0-b748f1f9fe41.png)


final_mask=mask+mask_white<br>
final_result=cv2.bitwise_and(img,img,mask=final_mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(final_mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(final_result)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940851/175256930-9ae771e4-4cb7-43ca-bf39-68b2dbc07361.png)


blur=cv2.GaussianBlur(final_result,(7,7),0)<br>
plt.imshow(blur)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/97940851/175257079-4bb9e433-07be-4e17-a7df-43fbac0010f6.png)


#12. Write a program to perform airthmetic operation on image<br>

import cv2<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>

#Read image file<br>
img1=cv2.imread('image1.jpg')<br>
img2=cv2.imread('image2.jpg')<br>

#numpy addition on image<br>
fimg1 = img1 + img2<br>
plt.imshow(fimg1)<br>
plt.show()<br>

#saving the output image<br>
cv2.imwrite('output.jpg',fimg1)<br>
fimg2 = img1 - img2<br>
plt.imshow(fimg2)<br>
plt.show()<br>
#saving<br><br>
cv2.imwrite('output.jpg',fimg2)<br>
fimg3 = img1 * img2<br>
plt.imshow(fimg3)<br>
plt.show()<br>
#saving<br>
cv2.imwrite('output.jpg',fimg3)<br>
fimg4 = img1 / img2<br>
plt.imshow(fimg4)<br>
plt.show()<br>
#saving<br>
cv2.imwrite('output.jpg',fimg4)<br>

#OUTPUT

![image](https://user-images.githubusercontent.com/97940851/175271361-f69fd056-0c9f-48de-9f0e-58f179e3165a.png)

![image](https://user-images.githubusercontent.com/97940851/175271547-755682e2-fb06-415c-becb-c9dfc61547b8.png)

![image](https://user-images.githubusercontent.com/97940851/175271715-3e037c18-5be8-4457-9ce2-2f77386b4f49.png)

![image](https://user-images.githubusercontent.com/97940851/175272011-17225891-481f-445d-b47e-1fb7804c5997.png)



****
import cv2<br>
img=cv2.imread("dog.jpg")<br>
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)<br>
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)<br>
lab=cv2.cvtColor(img,cv2.COLOR_BGR2LAB)<br>
hls=cv2.cvtColor(img,cv2.COLOR_BGR2HLS)<br>
yuv=cv2.cvtColor(img,cv2.COLOR_BGR2YUV)<br>
cv2.imshow("GRAY image",gray)<br>
cv2.imshow("HSV image",hsv)<br>
cv2.imshow("LAB image",lab)<br>
cv2.imshow("HLS image",hls)<br>
cv2.imshow("YUV image",yuv)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br><br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940851/175275459-1038aabc-f2e2-48d4-832e-4818794576d7.png)

![image](https://user-images.githubusercontent.com/97940851/175275565-e98518fb-4310-4ae7-9121-312f769a1789.png)

![image](https://user-images.githubusercontent.com/97940851/175275777-13baace2-7b44-40e2-8fca-601994e1dd4f.png)

![image](https://user-images.githubusercontent.com/97940851/175275902-3fdd3a34-d608-4f77-85c8-f3164238cb19.png)

![image](https://user-images.githubusercontent.com/97940851/175275976-0d96f5e4-beb2-4d92-b5b6-714205902ea2.png)



#13. Program to create an image using
import numpy as np<br>
from PIL import Image<br>
array=np.zeros([100,200,3],dtype=np.uint8)<br>
array[:,:100]=[255,130,0]<br>
array[:,100:]=[0,0,255]<br>
img=Image.fromarray(array)<br>
img.save('IMAGES.jpg')<br>
img.show()<br>
c.waitKey(0)<br><br>

**output**

![image](https://user-images.githubusercontent.com/97940851/175283707-b07903e6-eeae-4838-85e7-bd7f7177f98c.png)


#14. Bitwise Operator
import cv2<br>
import matplotlib.pyplot as plt<br>
image1=cv2.imread('images1.jpg',1)<br>
image2=cv2.imread('images1.jpg')<br>
ax=plt.subplots(figsize=(15,10))<br>
bitwiseAnd=cv2.bitwise_and(image1,image2)<br>
bitwiseOr=cv2.bitwise_or(image1,image2)<br>
bitwiseXor=cv2.bitwise_xor(image1,image2)<br>
bitwiseNot_img1=cv2.bitwise_not(image1)<br>
bitwiseNot_img2=cv2.bitwise_not(image2)<br>
plt.subplot(151)<br>
plt.imshow(bitwiseAnd)<br>
plt.subplot(152)<br>
plt.imshow(bitwiseOr)<br>
plt.subplot(153)<br>
plt.imshow(bitwiseXor)<br>
plt.subplot(154)<br>
plt.imshow(bitwiseNot_img1)<br>
plt.subplot(155)<br>
plt.imshow(bitwiseNot_img2<br>
cv2.waitKey(0)<br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940151/178716572-7b20a434-3c8a-4303-94b0-678fc92fa579.png)


#15. Blurring Image

#importing libraries<br>
import cv2<br>
import numpy as np<br>
image=cv2.imread('image1.jpg')<br>
cv2.imshow('Original Image',image)<br>
cv2.waitKey(0)<br>
#GaussianBlur<br>
Gaussian=cv2.GaussianBlur(image,(7,7),0)<br>
cv2.imshow('Gaussian Blurring',Gaussian)<br>
cv2.waitKey(0)<br>
#Median blur<br>
median=cv2.medianBlur(image,5)<br>
cv2.imshow('Median Blurring',median)<br>
cv2.waitKey(0)<br>
#Bilateral Blur<br>
bilateral=cv2.bilateralFilter(image,9,75,75)<br>
cv2.imshow('Bilateral Blurring',bilateral)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940151/178716959-0bb3e850-a70e-4fe9-b1f6-1012c7d5b5c0.png)
![image](https://user-images.githubusercontent.com/97940151/178717094-f8a9952d-ccf2-4915-833d-3a5edb4a5ee1.png)
![image](https://user-images.githubusercontent.com/97940151/178717229-c0361aa8-5a84-4966-a8a2-7a603500dbe5.png)
![image](https://user-images.githubusercontent.com/97940151/178717319-4bcafd27-5dfb-4c75-93b5-6d5d5bed7e53.png)
<br>




#16.Image Enhancement<br>

from PIL import Image<br>
from PIL import ImageEnhance<br>
image=Image.open('lotus.jpg')<br>
image.show()<br>
enh_bri=ImageEnhance.Brightness(image)<br>
brightness=1.5<br>
image_brightened=enh_bri.enhance(brightness)<br>
image_brightened.show()<br>
enh_col=ImageEnhance.Color(image)<br>
color=1.5<br>
image_colored=enh_col.enhance(color)<br>
image_colored.show()<br>
enh_con=ImageEnhance.Contrast(image)<br>
contrast=1.5<br>
image_contrasted=enh_con.enhance(contrast)<br>
image_contrasted.show()<br>
enh_sha=ImageEnhance.Sharpness(image)<br>
sharpness=3.0<br>
image_sharped=enh_sha.enhance(sharpness)<br>
image_sharped.show()<br>

**OUTPUT**

![image](https://user-images.githubusercontent.com/97940151/178718032-e69f77f4-8d44-44f7-a6a2-654234c06aa4.png)
![image](https://user-images.githubusercontent.com/97940151/178718210-a328abb6-6c2b-45e2-aa0c-2b60cc55d8d7.png)
![image](https://user-images.githubusercontent.com/97940151/178718283-77c533f8-ce90-42ad-ad82-1c863c9e103e.png)
![image](https://user-images.githubusercontent.com/97940151/178718354-d100b415-5363-41c5-b1e0-d7d1f6d23e0e.png)
![image](https://user-images.githubusercontent.com/97940151/178718423-2ade8460-afee-4b4b-a253-6b566b0b0e77.png)


#17.Morphological Operation

import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
from PIL import Image,ImageEnhance<br>
img=cv2.imread('img1.jpg',0)<br>
ax=plt.subplots(figsize=(20,10))<br>
kernel=np.ones((5,5),np.uint8)<br>
opening=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)<br>
closing=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)<br>
erosion=cv2.erode(img,kernel,iterations=1)<br>
dilation=cv2.dilate(img,kernel,iterations=1)<br>
gradient=cv2.morphologyEx(img,cv2.MORPH_GRADIENT,kernel)<br>
plt.subplot(151)<br>
plt.imshow(opening)<br>
plt.subplot(152)<br>
plt.imshow(closing)<br>
plt.subplot(153)<br>
plt.imshow(erosion)<br>
plt.subplot(154)<br>
plt.imshow(dilation)<br>
plt.subplot(155)<br>
plt.imshow(gradient)<br>
cv2.waitKey(0)<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940151/178718749-996313ad-3845-4f3d-9cb5-fb4ccbc68567.png)


<br>
<br>
#18. Develop the program to 1.read 2.write 3.display the image?<br>
import cv2<br>
OriginalImg=cv2.imread('i.jpg')<br>
GrayImg=cv2.imread('i.jpg',0)<br>
isSaved=cv2.imwrite('E:/i.jpg',GrayImg)<br>
cv2.imshow('Display Original Image',OriginalImg)<br>
cv2.imshow('Display Grayscale Image',GrayImg)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
if isSaved:<br>
    print('The image is successfully saved.')<br>

<br>
<br>
#19. Slicing with background?<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('i.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
            z[i][j]=image[i][j]<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing with background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>
<br>
<br>
OUTPUT:<br>
![image](https://user-images.githubusercontent.com/97940151/178708133-67df44c4-f8b9-4878-b801-76f3dedb0de5.png)



#20. Image without bachground?<br>

import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('i.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
     if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
            z[i][j]=0<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing w/o background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>
OUTPUT:<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/178707239-8ee25570-0cc2-44fc-aa1e-0a080d19e05c.png)

















