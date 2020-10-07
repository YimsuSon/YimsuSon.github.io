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

1.iOS Basic, Label and Button 만들기


<br/>


오늘은 Label 과 button 을 만드는 방법에 대해 배워 보도록 하겠습니다.
Label은 정보가 담겨있는 텍스트상자이구요, 이것은 class 입니다. class 가 뭐냐구요? 

<br/>

클래스는 여러 변수를 담을 수 있는 상자 입니다
여기서 변수는 데이터를 적어 놓는 종이  입니다.  예를 들어 1은 number다 라는 데이터를 저장하고 싶을때 var a  = 1 이라고 코드를 적으면 컴퓨터는 number 라는 종이에는 1이 적혀져있구나 라고 인식을 하게 됩니다. 그래서 다음에 number를 입력하게되면 컴퓨터는 1이 라는 정보도 같이 불러오게 되죠.
그러면 여러개의 변수들을 반복해서 사용해야하는 경우에 일일히 적어서 사용하게되면 번거로워지기 때문에 class라는 상자를 만들어 여기에 변수들을 담아 놓게 되는것죠.


<br/>


그러면 우선 iOS 프로젝트를 만들어 보도록 하겠습니다. Create a New Xcode project 라는 부분을 클릭해주시구요. Single View App을 클릭한 다음 next를 누르고  프로젝트 이름은 Hello, World로 하겠습니다.

<br>

Team 의 계정을 생성해주시고 Organization Name과 Organization Identifier 를 채워주세요. 
여기서 중요한부분은 User Interface 에서 Swift UI 가 아닌 Storyboard를 설정해주는것입니다. 
Use Core Data 부분의 체크를 없애주시고 next를 누르게되면 새로운 프로젝트가 만들어 집니다.
처음 나타나는 이 화면을 스토리보드라고 합니다  여기에서 오른쪽 상단에 있는 5개의 버튼중 + 버튼이 Library 들을 모아 놓은 버튼입니다

<br/>


이 Library는 안에 여러가지 기능들을 모아놓은 도구상자로 Shif + Command + L 단축키를 누르게 되면 창이 나타나게 됩니다. 여기서 Label 을 입력해주시고  스토리보드에 있는 휴대폰 모양의 씬으로 드래그 앤 드랍을 해주시면 가이드라인이 생기면서 Label 을 위치시킬수 있습니다. 

<br/>

여기서 오른쪽 상단의 5개 버튼중 가장 오른쪽에 있는 버튼을 누르게되면 Attribute inspector 창이 열리게됩니다 만약 라벨을 클릭하지 않았을경우 아무것도 표시가 되지 않습니다, 여기서 5번째에 있는 버튼을 클릭하고 Hello, World 를 입력후 Enter를 누르면 씬에 있는 라벨이 바뀌게 됩니다.
글씨가 바뀌면서 위치가 애매해지게 되었는데요 이것을 중앙에 배치시키기위해 우측 하단에 있는 버튼 중 Align 버튼을 클릭한뒤 horizontally in container 버튼을 체크하게되면 가로 축에서 중앙에 위치하게되고 vertically in container 버튼을 누르게 되면 세로 축에서 중앙에 위치하게 됩니다.

<br/>


다음으로는 button 을 추가해보도록 하겠습니다. 
Shift + Command + L 단축키를 눌러주시고 Button 을 입력해서 드래그 앤 드랍을 해줍니다 버튼을 왼쪽 하부에 위치시키고 크기를 키워줍니다. 오른쪽 하부에 3번째 아이콘은 constrain 을 설정하는곳입니다. 제약을 설정하게되면 제약만큼 버튼이 휴대폰의 크기에 맞춰지게 됩니다. 왼쪽,오른쪽,아래 제약을 설정한후 크기를 60으로 맞추어줍니다. 

<br/>
이제 버튼의 이름을 변경할수가있는데 더블클릭해서 change label 이라고 바꿔줍니다. 이제 이버튼을 터치하게되면 Hello world로 라벨이 업데이트되게 됩니다 이 기능을 구현하기위해 코드와 버튼을 연결해주어야합니다. 

<br/>

왼쪽에 ViewController.swift라는 파일을 클릭하게되면 코드가 들어있습니다. 다시 Main.storyboard로 돌아와서 오른쪽상단의 editor option을 클릭하고 assitant 를 클릭하게되면 코드 ViewController 파일이 열리게 됩니다

<br/>


씬에서 label을 선택한다음 control 키를 누르면서 drag and drop 을 하게되면 팝업이 표시되게 됩니다. 이 팝업은 컨넥션 패널이라고 부르게 됩니다. 이름을 label 이라 입력하고 connect 버튼을 누르게 되면 연결이 완료됩니다  이제 코드에서 label 이라는 Outlet 을 통해서 씬에 접근을 할 수 있게 됩니다.

<br/>

outlet은 UILabel 의 텍스트 업데이트, UIView의 배경이미지 설정, UIStepper의 현재값을 얻는 작업 등을 할 수 있습니다
버튼을 터치했을때 실행 할 수있는 코드를 구현하고싶다면 action으로 연결합니다.

<br/>

버튼을 클릭하고 control 키를 누른뒤  코드창으로 드래그 앤 드랍을 합니다 이번에는 outlet 이아닌 action으로 바꿔주고 updatelable로 이름을 입력합니다 그러면  클래스에 메소드가 추가됩니다. 
여기서 잠깐, 함수는 특정한 명령을 반복적으로 하는 코드의 집합이고 메소드는 class에 내부에 정의된 함수 입니다 

<br/>

이 메소드는 버튼을 탭할때마다 반복적으로 호출이됩니다 여기에서 label을 업데이트하는 코드를 구현하도록 하겠습니다 label은 text라는 속성을 가지고 있고 여기에 원하는 문자열 “This is first app”을 저장하면 화면에 표시된 문자열이 변경됩니다


<br/>

  
이제 빌드 단축키 command + B를 누르게되면 빌드가 실행이되는데 succeeded가 되어야 시뮬레이터가 실행를 실행할수있습니다.
다음으로 command + R키를 누르게되면 시뮬레이터가 실행이되게 됩니다.여기에서 change label을 누르게 된다면 “hello world!”에서  “this is first app”으로 label이 바뀌게됩니다 


<br/>



이것으로 가장 기본적인 앱이 만들어졌습니다. 여기에 기능을 추가시킨다면 여러분들만의 어플리케이션을 만들수 있게 됩니다. 그럼 오늘한 과정을 요약후 첫번째강의를 마무리 하도록 하겠습니다.


















<br/>
Label은 정보가 담겨있는 텍스트상자


<br/>
클래스는 여러 변수를 담을 수 있는 상자 입니다


<br/>
변수는 데이터를 적어 놓는 종이 


<br/>
IBOutlet은 UILabel 의 텍스트 업데이트, UIView의 배경이미지 설정, UIStepper의 현재값을 얻는 작업 등을 할 수 있습니다


<br/>
IBAction은 이벤트( ex)버튼 )를 터치했을때 실행 할 수있는 코드를 구현합니다


<br/>
함수는 특정한 명령을 반복적으로 하는 코드의 집합


<br/>
메소드는 class에 내부에 정의된 함수
<br/>


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

ShortcutKey
<br/>

``` c
Library = Shif + Command + L
Build = command + B
Run simulator = comman + R



// <iframe width="1000" height="625" src="https://www.youtube.com/embed/etZpWBEeIqk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

``` 


