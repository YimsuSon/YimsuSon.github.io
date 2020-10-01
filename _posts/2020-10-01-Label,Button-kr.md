---
title: 1.iOS Basic, Label and Button 만들기
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


Label은 정보가 담겨있는 텍스트상자

클래스는 여러 변수를 담을 수 있는 상자 입니다
변수는 데이터를 적어 놓는 종이 


utlet은 UILabel 의 텍스트 업데이트, UIView의 배경이미지 설정, UIStepper의 현재값을 얻는 작업 등을 할 수 있습니다

action으로 연결합니다. 이벤트( ex)버튼 )를 터치했을때 실행 할 수있는 코드를 구현

함수는 특정한 명령을 반복적으로 하는 코드의 집합

메소드는 class에 내부에 정의된 함수


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
