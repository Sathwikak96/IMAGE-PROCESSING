**1. Develop a program to display a grayscale image using read and write operation?**<br>
<br>
pip install opencv-python<br>
import cv2<br>
img=cv2.imread('F1.jfif',0)<br>
cv2.imshow('image',img)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
<br>
**OUTPUT**:-<br>
![image](https://user-images.githubusercontent.com/97940151/174038089-0609c4b5-63a7-4835-ae9a-b3eebab4484b.png)<br>
--------------------------------------------------------------------------------------<br>
**2. Develop a program to display the image using matplotlib?** <br>
<br>
import matplotlib.image as mping<br>
import matplotlib.pyplot as plt<br>
img=mping.imread('F1.jfif')<br>
plt.imshow(img)<br>
<br>
**OUTPUT:-**<br>
![image](https://user-images.githubusercontent.com/97940151/174039132-01d337a3-80c1-4204-bfd9-cb5a1514dab7.png)<br>
-------------------------------------------------------------------------------------<br>
**3. Develop a program to perform a linear transformation using rotation?**<br>
<br>
import cv2<br>
from PIL import Image<br>
img=Image.open('F1.jfif')<br>
img=img.rotate(180)<br>
img.show()<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
<br>
**OUTPUT:-**<br>
![image](https://user-images.githubusercontent.com/97940151/174040352-3f9bea71-216a-4061-815f-cab7a428f5d5.png)<br>
--------------------------------------------------------------------------------<br>
**4. Develop a program to convert color tree to RCB color values?**<br>
<br>
from PIL import ImageColor<br>
img1=ImageColor.getrgb("yellow")<br>
print(img1)<br>
img2=ImageColor.getrgb("red")<br>
print(img2)<br>                           
img3=ImageColor.getrgb("pink")<br>
print(img3)<br>
<br>
**OUTPUT:-**<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174041325-6755a879-4216-49e7-ae20-13a5c31b9320.png)<br>
------------------------------------------------------------------------------------------------<br>
**5.Write a program to create using a color?**<br>
<br>
from PIL import Image<br>
img=Image.new('RGB',(200,400),(255,0,0))<br>
img.show()<br>
<br>
**OUTPUT:-**<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/174042123-12f038b4-ff4f-4e51-8af6-d2f0690fccb3.png)<br>
---------------------------------------------------------------------------------------------------<br>
**6. Develop a program to visualize the image using various color spaces?**<br>
<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
import numpy as np<br>
img=cv2.imread('c1.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<br>
plt.imshow(img)<br>
plt.show()<br>
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
plt.imshow(img)<br>
plt.show()<br>
<br>
**OUTPUT:-**<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/179970122-ee39d298-9289-4cbb-b3d0-7bc1b1e8eb89.png)<br>
![image](https://user-images.githubusercontent.com/97940151/179970205-be5323c5-c4c6-4469-9834-86d28d4575c8.png)<br>
![image](https://user-images.githubusercontent.com/97940151/179970287-1a369ef1-e899-4cb7-82c8-57bb125d68d1.png)<br>
----------------------------------------------------------------------------------------------------------<br>
**7. Develop a program to display the image attributes?**<br>
<br>
from PIL import Image<br>
image=Image.open('p1.jpg')<br>
print("Filename:",image.filename)<br>
print("Format:",image.format)<br>
print("Mode:",image.mode)<br>
print("Size:",image.size)<br>
print("Width:",image.width)<br>
print("Height:",image.height)<br>
image.close()<br>
<br>
**OUTPUT:-**<br>
<br>
Filename: p1.jpg<br>
Format: JPEG<br>
Mode: RGB<br>
Size: (225, 225)<br>
Width: 225<br>
Height: 225<br>
------------------------------------------------------------------------------------------------<br>
**8. Convert the original image to gray scale and then to binary?**<br>
<br>
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
**OUTPUT:-**<br>
![image](https://user-images.githubusercontent.com/97940151/180175552-8e6759f6-8733-487a-93ef-f50c906e72ce.png)<br>
![image](https://user-images.githubusercontent.com/97940151/180175697-ee52fe3b-55bb-47cd-a604-37d136e01002.png)<br>
![image](https://user-images.githubusercontent.com/97940151/180176131-4b92090b-28d7-4fd1-8627-e29950d8b3e7.png)<br>
-------------------------------------------------------------------------------------------------<br>
**9. Resize the original image?**<br>
<br>
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
**OUTPUT:-**<br>
original image length width (168, 299, 3)<br>
Resized image length width (160, 150, 3)<br>
![image](https://user-images.githubusercontent.com/97940151/180202210-ebea768e-299d-4a01-958b-8c4a52f1cfa7.png)<br>
![image](https://user-images.githubusercontent.com/97940151/180202312-c5d32b2b-55bd-4aa8-adf7-8ccd20940988.png)<br>
-------------------------------------------------------------------------------------------------------<br>
 **10. Develop a program to read image using URL ?**<br>
 <br>
 url from skimage import io<br>
 import matplotlib.pyplot as plt<br>
 url='https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ3VyCF39_x0MhTZema9w9qnFPw6SgAAnY0lA&usqp=CAU'<br>
 image=io.imread(url)<br>
 plt.imshow(image)<br>
 plt.show()<br>
 **OUTPUT:-**<br>
 <br>
![image](https://user-images.githubusercontent.com/97940151/180203529-8089d13e-c72f-4765-acb0-5076373cdb5a.png)<br>
----------------------------------------------------------------------------------------------------------------<br>
**11. Write a program to mask and blur the image?**<br>
<br>
import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>
img=cv2.imread('fish.jpg')<br><br>
plt.imshow(img)<br>
plt.show()<br>
![image](https://user-images.githubusercontent.com/97940851/175256088-534b41d1-7204-4e74-8ffa-b2e07fd3a6a3.png)<br>
<br>
<br>
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
![image](https://user-images.githubusercontent.com/97940851/175256433-cd6a66bd-0eec-42ed-9281-3a002ad19731.png)<br>
<br>
<br>
light_white=(0,0,200)<br>
dark_white=(145,60,255)<br>
mask_white=cv2.inRange(hsv_img,light_white,dark_white)<br>
result_white=cv2.bitwise_and(img,img,mask=mask_white)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask_white,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result_white)<br>
plt.show()<br>
<br>
<br>
![image](https://user-images.githubusercontent.com/97940851/175256779-ede4be6e-d028-445b-8ec0-b748f1f9fe41.png)<br>
<br>
<br>
final_mask=mask+mask_white<br>
final_result=cv2.bitwise_and(img,img,mask=final_mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(final_mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(final_result)<br>
plt.show()<br>
<br>
![image](https://user-images.githubusercontent.com/97940851/175256930-9ae771e4-4cb7-43ca-bf39-68b2dbc07361.png)<br>
<br>
<br>
blur=cv2.GaussianBlur(final_result,(7,7),0)<br>
plt.imshow(blur)<br>
plt.show()<br>
<br>
![image](https://user-images.githubusercontent.com/97940851/175257079-4bb9e433-07be-4e17-a7df-43fbac0010f6.png)<br>
---------------------------------------------------------------------------------------------------------------<br>
**12.Write a program to perform airthmetic operation on image**<br>
<br>
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
**OUTPUT:-**<br>
 <br>
![image](https://user-images.githubusercontent.com/97940151/180200678-85e7c451-385e-4ffb-b6ac-67470155ff0f.png)<br>
![image](https://user-images.githubusercontent.com/97940151/180200746-f01a5689-587e-4b34-ac4a-4b9935287029.png)<br>
![image](https://user-images.githubusercontent.com/97940151/180200816-8d61c20b-4529-4cef-a2fe-0e079ebf1e91.png)<br>
![image](https://user-images.githubusercontent.com/97940151/180200883-ec735242-c664-4d90-8ee2-f3d0f128af81.png)<br>
---------------------------------------------------------------------------------------------------------------<br>
**13.Develop the program to changeb the image to different Colour space?**<br>
 <br>
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
cv2.destroyAllWindows()<br>
<br>
**OUTPUT:-**<br>
 <br>
![image](https://user-images.githubusercontent.com/97940151/178719420-36dca750-88a2-460d-b71f-de421bb36baf.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178719500-da5cfb95-7e89-4aef-b140-4b338f903d40.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178719594-89d6f8a9-5a63-41d9-a2ab-434281dd9e41.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178719671-b40d80dc-a9e6-4784-ba2c-f065f90f22a6.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178719747-a34268a3-d00d-4e53-ab9a-55f46387b662.png)<br>
--------------------------------------------------------------------------------------------------------------------<br>
**14. Program to create an image using 2D array?**<br>
<br>
import numpy as np<br>
from PIL import Image<br>
array=np.zeros([100,200,3],dtype=np.uint8)<br>
array[:,:100]=[255,130,0]<br>
array[:,100:]=[0,0,255]<br>
img=Image.fromarray(array)<br>
img.save('IMAGES.jpg')<br>
img.show()<br>
c.waitKey(0)<br>
**OUTPUT:-**<br>
<br>
![image](https://user-images.githubusercontent.com/97940851/175283707-b07903e6-eeae-4838-85e7-bd7f7177f98c.png)<br>
**15. Write a program to perform the bitwise operation?**<br>
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
**OUTPUT:-**<br>
 <br> 
![image](https://user-images.githubusercontent.com/97940151/183875797-d73963a6-0bc1-454a-bcb6-061f9a37de8a.png)<br>
**16. Develop an image usingn Blurring method?**<br>
<br>
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
**OUTPUT:-**<br>
  <br>
![image](https://user-images.githubusercontent.com/97940151/178968682-ef4d317c-df76-4107-a8ee-91f72acddc6f.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178969106-69457483-6e75-42e6-a082-0b07d6bc5cff.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178969211-c56e57db-a216-4653-8a81-7a7d1b2d3732.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178969294-165f3437-5c75-4988-8d87-20fc949862de.png)<br>
**17. Write a program to perform Image Enhancement?**<br>
  <br>
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
**OUTPUT:-**<br>
  <br>
![image](https://user-images.githubusercontent.com/97940151/181207385-835e868f-1c38-4758-a438-e65a60aa9c18.png)<br>
![image](https://user-images.githubusercontent.com/97940151/181207586-85aae0fa-2c9e-4f36-8676-8c05e2fc3868.png)<br>
![image](https://user-images.githubusercontent.com/97940151/181207741-77dfd707-6eff-4bd4-afeb-bd14d2c41dd9.png)<br>
![image](https://user-images.githubusercontent.com/97940151/181208035-20590cd9-bf0a-44ff-937d-6a406d8b2997.png)<br>
**18.Write a program to perform Morphological Operation?**<br>
  <br>
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
**OUTPUT:-**<br>
  <br>
![image](https://user-images.githubusercontent.com/97940151/178718749-996313ad-3845-4f3d-9cb5-fb4ccbc68567.png)<br>
**19. Develop the program to 1.read 2.write 3.display the image?**<br>
  <br>
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
**OUTPUT:-**<br>
![image](https://user-images.githubusercontent.com/97940151/180195224-0e99e2bf-c680-4574-9df5-b6857bf62de4.png)<br>
![image](https://user-images.githubusercontent.com/97940151/180195592-ff4db8c6-c431-4f54-9277-79afb4354831.png)<br>
**20.Write a program to Slicing the image with background?**<br>
  <br>
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
**OUTPUT:-**<br>
  <br>
![image](https://user-images.githubusercontent.com/97940151/178708133-67df44c4-f8b9-4878-b801-76f3dedb0de5.png)<br>
**21. Write a program to slicing the Image without bachground?**<br>
  <br>
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
**OUTPUT:-**<br>
<br>
![image](https://user-images.githubusercontent.com/97940151/178707239-8ee25570-0cc2-44fc-aa1e-0a080d19e05c.png)<br>
**histogram?**<br>
 **_________________**<br>
  <br>
import numpy as np<br>
import skimage.color<br>
import skimage.io<br>
import matplotlib.pyplot as plt<br>
#matplotlib widget<br>
#read the image of a plant seedling as grayscale from the outset<br>
image = skimage.io.imread(fname="img3.jpg", as_gray=True)<br>
image1 = skimage.io.imread(fname="img3.jpg")<br>
#display the image<br>
fig, ax = plt.subplots()<br>
plt.imshow(image, cmap="gray")<br>
plt.show()<br>
#display the image<br>
fig, ax = plt.subplots()<br>
plt.imshow(image1, cmap="gray")<br>
plt.show()<br>
#create the histogram<br>
histogram, bin_edges = np.histogram(image, bins=256, range=(0, 1))<br>
#configure and draw the histogram figure<br>
plt.figure()<br>
plt.title("Grayscale Histogram")<br>
plt.xlabel("grayscale value")<br>
plt.ylabel("pixel count")<br>
plt.xlim([0.0, 1.0])  # <- named arguments do not work here<br>
plt.plot(bin_edges[0:-1], histogram)  # <- or here<br>
plt.show()<br>
**OUTPUT:-**<br>
  <br>
![image](https://user-images.githubusercontent.com/97940151/178963447-d34d640f-6a57-44e8-a083-0f0b9292fcf5.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178963522-d9288839-8cd9-410e-972b-f8cb9b2b4daf.png)<br>
![image](https://user-images.githubusercontent.com/97940151/178963608-093033d6-0d51-4d14-8720-4b2300381c33.png)<br>
**22. Program to perform basic image data analysis using intensity transformation?**<br>
  <br>
  a.Image negative<br>
  b.Log transformation<br>
  c.Gamma correction<br>
# a. <br>
   import imageio<br>
   import matplotlib.pyplot as plt<br>
   import warnings<br>
   import matplotlib.cbook<br>
   warnings.filterwarnings("ignore",category=matplotlib.cbook.mplDeprecation)<br>
   pic=imageio.imread('img3.jpg')<br>
   plt.figure(figsize=(6,6))<br>
   plt.imshow(pic);<br>
   plt.axis('off');<br>
    ![image](https://user-images.githubusercontent.com/97940151/179962983-7bbc1605-df55-4f47-85aa-a8ec0befb4f4.png)<br>
   negative=255-pic<br>
   plt.figure(figsize=(6,6))<br>
   plt.imshow(negative);<br>
   plt.axis('off');<br>
OUTPUT:-<br>
![image](https://user-images.githubusercontent.com/97940151/179963159-6f6da6b6-2be8-40d4-b037-58a510d6cde5.png)<br>
# b. <br>
    import imageio<br>
    import numpy as np<br>
    import matplotlib.pyplot as plt<br>
    pic=imageio.imread('img3.jpg')<br>
    gray=lambda rgb:np.dot(rgb[...,:3],[0.299,0.587,0.114])<br>
    gray=gray(pic)<br>
    max_=np.max(gray)<br>
    def log_transform():<br>
        return(255/np.log(1+max_))*np.log(1+gray)<br>
    plt.figure(figsize=(5,5))<br>
    plt.imshow(log_transform(),cmap=plt.get_cmap(name='gray'))<br>
    plt.axis('off');
  **OUTPUT:-**<br>
  ![image](https://user-images.githubusercontent.com/97940151/179963780-9a1a1619-def0-4cf8-98d3-3a3032762ffc.png)<br>
# c.<br> 
   import imageio<br>
   import matplotlib.pyplot as plt<br>
   pic=imageio.imread('img3.jpg')<br>
   gamma=2.2<br>
   gamma_correction=((pic/255)**(1/gamma))<br>
   plt.figure(figsize=(5,5))<br>
   plt.imshow(gamma_correction)<br>
   plt.axis('off'); <br> 
  **OUTPUT:-**<br>
 ![image](https://user-images.githubusercontent.com/97940151/179963905-6e9bda49-e5de-4957-b40b-d85332569be9.png)<br>
**23. Program to perform image manipulation?**<br>
  <br>
a. Sharpness<br>
b. flipping<br>
c. Cropping<br>
# a. <br>
from PIL import Image<br>
from PIL import ImageFilter<br>
import matplotlib.pyplot as plt<br>
my_image=Image.open('t1.jpg')<br>
sharp=my_image.filter(ImageFilter.SHARPEN)<br>
sharp.save('E:/image_sharpen.jpg')<br>
sharp.show()<br>
plt.imshow(sharp)<br><br>
plt.show()<br>
OUTPUT:-<br>
  <br>
![image](https://user-images.githubusercontent.com/97940151/179965900-4cb4522a-e238-4db0-a573-2537282775b3.png)<br>
# b.<br>
import matplotlib.pyplot as plt<br>
img=Image.open('t1.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>
flip=img.transpose(Image.FLIP_LEFT_RIGHT)<br>
flip.save('E:/image_flip.jpg')<br>
plt.imshow(flip)<br>
plt.show()<br><br>
OUTPUT:-<br>
  <br>
![image](https://user-images.githubusercontent.com/97940151/179966024-7aa62a81-3816-4939-b7b5-fd170e83dc3a.png)<br>
![image](https://user-images.githubusercontent.com/97940151/179966091-357e4b10-1c3d-4607-820c-21b410c4c55a.png)<br>
# c.<br>
from PIL import Image<br>
import matplotlib.pyplot as plt<br>
im=Image.open('t1.jpg')<br>
width,height=im.size<br>
im1=im.crop((50,25,175,200))<br>
im1.show()<br>
plt.imshow(im1)<br>
plt.show()<br>
**OUTPUT:-**<br>
![image](https://user-images.githubusercontent.com/97940151/179966254-6f526475-ddfe-46e3-a9f6-832df99ce58c.png)<br>
**24.Generate a matrix to display the image?**<br>
#First import the required Python Libraries<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
from skimage import img_as_uint<br>
from skimage.io import imshow, imread<br>
from skimage.color import rgb2hsv<br>
from skimage.color import rgb2gray<br>
array_1 = np.array([[255, 0,17],<br> 
                    [100,0, 255],<br>
                    [255,0,35]])<br>
imshow(array_1);<br>
**OUTPUT:-**<br>
![image](https://user-images.githubusercontent.com/97940151/181440039-bb14a98e-7842-4ada-8fea-0902f246d266.png)<br>
**25. Generate a matrix to display the gray image?**<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
from skimage import img_as_uint<br>
from skimage.io import imshow, imread<br>
from skimage.color import rgb2hsv<br>
from skimage.color import rgb2gray<br>
array_1 = np.array([[255, 0,17], <br>
                    [100,0, 255],<br>
                    [255,0,35]])<br>
imshow(array_1,cmap='gray');<br>
**OUTPUT:-**<br>
![image](https://user-images.githubusercontent.com/97940151/181440540-b33c2069-8122-444c-bc1e-38198bde5551.png)<br>
**26. Write a code to read the image data in the form of matrix and find maximum,minimum,average and standard deviation?**<br>
**MAXIMUM:-**<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
array_colors = np.array([[[245, 20, 36], <br>
                         [10, 215, 30],<br>
                         [40, 50, 205]],<br>
                         [[70, 50, 10], <br>
                    [25, 230, 85],<br>
                    [12, 128, 128]],<br>
                    [[25, 212, 3], <br>
                    [55, 5, 250],<br>
                    [240, 152, 25]],<br>
                    ])<br>
plt.imshow(array_colors)<br>
np.max(array_colors)<br>
**OUTPUT:-**<br>
250<br>
![image](https://user-images.githubusercontent.com/97940151/181441254-5eee4e61-b295-4622-a611-6df54432a505.png)<br>
**MINIMUM:-**<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
array_colors = np.array([[[245, 20, 36], <br>
                         [10, 215, 30],<br>
                         [40, 50, 205]],<br>
                         [[70, 50, 10], <br>
                    [25, 230, 85],<br>
                    [12, 128, 128]],<br>
                    [[25, 212, 3],<br> 
                    [55, 5, 250],<br>
                    [240, 152, 25]],<br>
                    ])<br>
plt.imshow(array_colors)<br>
np.min(array_colors)<br>
**OUTPUT:-**<br>
3<br>
![image](https://user-images.githubusercontent.com/97940151/181441491-1af56639-ef76-4172-8100-29be3b0154eb.png)<br>
**AVERAGE:-**<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
array_colors = np.array([[[245, 20, 36], <br>
                         [10, 215, 30],<br>
                         [40, 50, 205]],<br>
                         [[70, 50, 10], <br>
                    [25, 230, 85],<br>
                    [12, 128, 128]],<br>
                    [[25, 212, 3], <br>
                    [55, 5, 250],<br>
                    [240, 152, 25]],<br>
                    ])<br>
plt.imshow(array_colors)<br>
np.average(array_colors)<br>
**OUTPUT:-**<br>
94.66666666666667<br>
![image](https://user-images.githubusercontent.com/97940151/181441736-9a32c7f5-c40e-4772-b6f8-00259470de30.png)<br>
**STANDARD DEVIATION:-**<br>
import numpy as np<br>
import matplotlib.pyplot as plt<br>
array_colors = np.array([[[245, 20, 36], <br>
                         [10, 215, 30],<br>
                         [40, 50, 205]],<br>
                         [[70, 50, 10], <br>
                    [25, 230, 85],<br>
                    [12, 128, 128]],<br>
                    [[25, 212, 3], <br>
                    [55, 5, 250],<br>
                    [240, 152, 25]],<br>
                    ])<br>
plt.imshow(array_colors)<br>
np.std(array_colors)<br>
**OUTPUT:-**<br>
87.50068782798436<br>
![image](https://user-images.githubusercontent.com/97940151/181442090-7b7999c6-def6-479a-82bf-d6ef128526f3.png)<br>
**27. Write a program to display the rectangular pattern?**<br>
#Python3 program for printing<br>
#the rectangular pattern<br>
 #Function to print the pattern<br>
def printPattern(n):<br>
    arraySize = n * 2 - 1;<br>
    result = [[0 for x in range(arraySize)]<br>
                 for y in range(arraySize)];<br>
    #Fill the values<br>
    for i in range(arraySize):<br>
        for j in range(arraySize):<br>
            if(abs(i - (arraySize // 2)) ><br>
               abs(j - (arraySize // 2))):<br>
                result[i][j] = abs(i - (arraySize // 2));<br>
            else:
                result[i][j] = abs(j - (arraySize // 2));<br>
    #Print the array<br>
    for i in range(arraySize):<br>
        for j in range(arraySize):<br>
            print(result[i][j], end = " ");<br>
        print("");<br>
#Driver Code<br>
n = 4;<br>
printPattern(n);<br>
**OUTPUT:-**<br>
3 3 3 3 3 3 3 <br>
3 2 2 2 2 2 3 <br>
3 2 1 1 1 2 3 <br>
3 2 1 0 1 2 3 <br>
3 2 1 1 1 2 3 <br>
3 2 2 2 2 2 3 <br>
3 3 3 3 3 3 3<br> 
---------------------------------------------------------------------------------------------------------------------------------------------------------<br>
**EDGE DETECTION**<br>
import cv2<br>
#Read the original image<br>
img = cv2.imread('p1.jpg')<br>
#Display original image<br>
cv2.imshow('Original', img)<br>
cv2.waitKey(0)<br>
#Convert to graycsale<br>
img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)<br>
#Blur the image for better edge detection<br>
img_blur = cv2.GaussianBlur(img_gray, (3,3), 0)<br>
#Sobel Edge Detection<br>
sobelx = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=1, dy=0, ksize=5) # Sobel Edge Detection on the X axis<br>
sobely = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=0, dy=1, ksize=5) # Sobel Edge Detection on the Y axis<br>
sobelxy = cv2.Sobel(src=img_blur, ddepth=cv2.CV_64F, dx=1, dy=1, ksize=5) # Combined X and Y Sobel Edge Detection<br>
#Display Sobel Edge Detection Images<br>
cv2.imshow('Sobel X', sobelx)<br>
cv2.waitKey(0)<br>
cv2.imshow('Sobel Y', sobely)<br>
cv2.waitKey(0)<br>
cv2.imshow('Sobel X Y using Sobel() function', sobelxy)<br>
cv2.waitKey(0)<br>
#Canny Edge Detection<br>
edges = cv2.Canny(image=img_blur, threshold1=100, threshold2=200) # Canny Edge Detection<br>
#Display Canny Edge Detection Image<br>
cv2.imshow('Canny Edge Detection', edges)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
OUTPUT:-<br>
![image](https://user-images.githubusercontent.com/97940151/186399471-9345bd31-8fdb-4d19-9e6d-0bf47d042c20.png)<br>
![image](https://user-images.githubusercontent.com/97940151/186399600-b0cfc9a8-8506-4d1f-a0a2-0d0c723360ee.png)<br>
![image](https://user-images.githubusercontent.com/97940151/186399691-6fcd1438-a75a-471b-ab2c-67257f3e6234.png)<br>
![image](https://user-images.githubusercontent.com/97940151/186399808-ef92efa4-daf1-4a63-a7d3-56a27b6ec4bc.png)<br>
![image](https://user-images.githubusercontent.com/97940151/186399886-a598ef49-6cc2-4972-a546-5f2bfba30680.png)<br>




