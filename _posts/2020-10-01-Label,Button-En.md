---
title: 1.iOS Basic, Let’s make Label and Button in IOS app
excerpt: iOS


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
  - iOS

tags:
  - iOS_Basic
  - "2020"
  - "2020.10"



---


Label = a view that displays one or more lines of informational text.  

Variable = The paper written about data.

Class = The carton which can contains lots of variable.

Function = The set of code that repeatly implement specific order.

Method = The function defined inside class.


IBOutlet = It could do the task that update the text of UILabel, set the background image of UIView and gain the present value of UIStepper etc.

IBAction = Embody the running code when you touch the event( ex) Button ).



<br/>
TodayCode
<br/>

``` swift

import UIKit

class ViewController: UIViewController {

    
    @IBOutlet weak var label: UILabel!
    
    
    @IBAction func updateLabel(_ sender: Any) {
        label.text = "Hello, iOS"
    }
    
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.
    }


}

```

<br/>

Shortcut Key
<br/>

``` c
Library = Shif + Command + L
Build = command + B
Run simulator = comman + R
``` 
