---
title: Arithmetic operation and logic operation of Video
excerpt: Computer Vision


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
tags: "blog"
categories:
  - Ai
---

### Arithmetic operation and logic operation of Video

<br/>
<br/>

### 1. Addition operation

``` c
dst(x,y) = saturate(src1(x,y)+src2(x,y))
```
- It Add the pixel value that exists on same position between two videos and Set the pixel value of video.
- If the value is more than 255, set the pixel value to 255.

``` c
cv2.add(src1, src2, dst=None, mask=None, dtype=None) -> dst
```

- src1 : (input) first video or schalar
- src2 : (input) second video or schalar
- dst : (output) result video of addition operation
- mask : mask video
- dtype : type of output video 


 
### 