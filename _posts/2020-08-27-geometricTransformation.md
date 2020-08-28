---
title: Geometric transformation
excerpt: ComputerVision


#최상위 사진
header:
  image: /assets/images/foo-bar-identity.jpg
  teaser: /assets/images/foo-bar-identity-th.jpg

gallery:
  - url: /assets/images/unsplash-gallery-image-1.jpg
    image_path: assets/images/unsplash-gallery-image-1-th.jpg
    alt: "placeholder image 1"
  - url: /assets/images/unsplash-gallery-image-2.jpg
    image_path: assets/images/unsplash-gallery-image-2-th.jpg
    alt: "placeholder image 2"
  - url: /assets/images/unsplash-gallery-image-3.jpg
    image_path: assets/images/unsplash-gallery-image-3-th.jpg
    alt: "placeholder image 3"
    


 #사이드바 설정 
sidebar:
  - title: "Role"
    nav: sidebar-sample

# 해당 글 목차
toc: true
toc_sticky: true

toc_label: "Yimsu's Blog"
toc_icon: "cog"


## 테그설정

categories:
  - ComputerVision
  - Portfolio

tags: "ComputerVision"

---

### Image filtering

<br/>
<br/>

### 1. Transformation of image and shear transition
- Meaning of geometric transformation
    - The task to change the whole image by altering arrangement of pixel composing image.
    - ex) Image registration, removal of geometric distortion, etc.
<br/>


![image](/assets/images/computervision/1-20200827.png)
<br/>

- Translation transformation
  - The transformation moving the image as specific size to horizontal or vertical direction.
  - It have to set the translation displacement of x-axis and y-axis 

<br/>

![image](/assets/images/computervision/2-20200827.png)

<br/>

- Affine transformation function

``` c

cv2.warpAffine(src, M, dsize, dst=None, flags=None, borderMode=None, borderValue=None) -> dst

```

- src : Input image
- M : 2 x 3 affine metrix
- dsize : Result image size
- dst : Output image
- flags : Interpolation type
- borderMode : Edge pixel expension method
- borderValue : default value is 0

<br/>

- Example of translation transformation of the image

![image](/assets/images/computervision/3-20200827.png)

<br/>


- Shear transformation 
  - It have to set each x-axis and y-axis.



