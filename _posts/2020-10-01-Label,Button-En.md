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
1.iOS Basic, Let’s make Label and Button in IOS app



<br/>


Today, we will learn how to make Label and Button.
Label is a text box with information, and this is class. What's class?


<br/>


A class is a box that can hold many variables.
Here, the variable is the paper that writes down the data. For example, if you want to save data that says 1 is number, if you write the code var a = 1, the computer recognizes that number is written on the number paper. So you enter the number, the computer will also get information 1.

So if you have to use multiple variables over and over again, you're going to have to write them down, and you're going to create a box called class, and you're going to put them in here.




<br/>

Let's start with the iOS project. Click Create a New Xcode project. Click the Single View App, then click next, and then name the project "Hello, World."

<br>


Please create an Team account and fill in Organization Name and Organization Identifier.
The important part here is setting up the Storyboard instead of Swift UI in the User Interface.
Remove the check from the Use Core Data section and click Next to create a new project.

This screen that first appears is called the storyboard. Here in the upper right corner, the + button of the five buttons is a collection of the Library.

<br/>

This Library is a toolbox with a collection of functions inside, and when you press the Shif + Command + L shortcut, a window appears. If you enter the label here and drag and drop it into the cell phone-shaped scene on the storyboard, you can position the label with guidelines.


<br/>

Here, pressing the button on the far right of the top five buttons opens the Attribute Inspector window. If you do not click the label, nothing will be displayed.

Here, click the button on the fifth, type "Hello, World," and press Enter to change the label on the scene.
As the letters changed, the position became ambiguous.


To center it, click the "Align" button on the bottom right, and then check the "horizon" button, and then it's centered on the horizontal axis, and when you press the "vertically in connector" button, it's centered on the longitudinal axis.


<br/>

Next, I'll add a button.
Press Shift + Command + L Shortcut and enter Button to drag and drop the button on the lower left corner and increase the size.

The third icon in the lower right corner is where you set the "confrain". If you set the restriction, the button will fit the size of your phone as much as you can. Set the left, right, and bottom constraints and set the size to 60.


<br/>
Now you can change the name of the button, but you can double-click it and change it to "change label."

Now when you touch this button, the label is updated to "Hello world". You need to connect the code and button to implement this function.



<br/>
If you click on the file "ViewController.swift" on the left, the code will be included. 

When you return to "Main.storyboard" again, click on "editor option" in the upper-right corner and click "assitant," the code "ViewController" file opens.

<br/>

Select label in the scene and drag and drop while pressing the control key, a pop-up is displayed.

This pop-up is called a connection panel.

Enter the name label and press the connect button to complete the connection.

Now you can access the scene through the outlet called label in the code.

<br/>

Outlets can update the text in UILabel, set the background image in UIView, and get the current value of UIStepper.
If you want to implement code that can be executed when the button is touched, connect it with action.


<br/>

Click the button, press the control key, and drag and drop to the code window. This time, replace it with "action" instead of "outlet" and enter the name "Updatable". This adds the method to the class.


Wait a minute, a function is a set of codes that repeat a specific command, and the method is a function defined internally in the class.


<br/>


This method is called repeatedly every time you tap a button. We will implement the code to update the label here.

The label has a property called text, and if you save the desired string "This is first app," the displayed string on the screen changes.


<br/>

Now, when you press the build shortcut command + B, the build will run, and the simulator will not be able to run until "successful".

Next press command + R to run the simulator.If you press change label here, the label changes from "hello world!" to "this is first app."


<br/>

This is how the most basic app was created. If you add a function to this, you can create your own application. Then I will summarize today's course and wrap up the first lecture.







<br/>
Label = a view that displays one or more lines of informational text.  

<br/>
Variable = The paper written about data.

<br/>
Class = The carton which can contains lots of variable.

<br/>
Function = The set of code that repeatly implement specific order.

<br/>
Method = The function defined inside class.

<br/>
IBOutlet = It could do the task that update the text of UILabel, set the background image of UIView and gain the present value of UIStepper etc.

<br/>
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
