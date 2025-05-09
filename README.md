# 1- to-1 RTC: Android App with SmartFloMeet Android Toolkit

Explore a Sample Android App Demonstrating SmartFloMeet Platform Video APIs and Android Toolkit for 1-to-1 Real-Time Communication (RTC)

Uncover the power of the SmartFloMeet platform's Video APIs (https://doc.smartflomeet.ttns.in/developer/video-api/server-api/) and Android Toolkit (https://doc.smartflomeet.ttns.in//developer/video-api/client-api/android-toolkit/) through this illustrative Android application. This app equips developers with the tools to fast-track their app development journey, allowing them to host the application on their own Android devices.

With this app, you can effortlessly create virtual rooms on-the-fly within the SmartFloMeet platform using REST calls. It harnesses Room credentials, such as Room ID, to seamlessly connect as a mobile client to the virtual Room. These Room credentials can also be conveniently shared with others, enabling collaborative real-time communication (RTC) sessions in the same virtual Room.


## 1. How to get started

### 1.1 Pre-Requisites

#### 1.1.1 App Id and App Key 


* Login to the SmartFloMeet Portal
* Create your Application Key
* Get your App ID and App Key delivered to your email


#### 1.1.2 Sample Android Client 

* Clone or download this repository [https://github.com/smartflomeet/One-to-One-Video-Call-Webrtc-Application-Sample-for-Android.git] 


#### 1.1.3 Test Application Server

You need to set up an Application Server to provision Web Service API for your Android Application to communicate enabling Video Session. 

To help you try our Android Application quickly, without having to set up Application Server, this Application is shipped pre-configured to work in a "try" mode with SmartFloMeet hosted Application Server i.e. https://demo.smartflomeet.ttns.in/. 

Our Application Server restricts a single Session Durations to 10 minutes and allows 1 moderator and not more than 3 participants in a Session.

Once you tried SmartFloMeet Android Sample Application, you may need to set up your own  Application Server and verify your Application to work with your Application Server. Refer to point 2 for more details on this.


#### 1.1.4 Configure Android Client 

* Open the App
* Go to WebConstants and change the following:
``` 
 /* To try the App with SmartFloMeet Hosted Service you need to set the kTry = true When you setup your own Application Service, set kTry = false */
     
     public  static  final  boolean kTry = true;
     
 /* Your Web Service Host URL. Keet the defined host when kTry = true */
 
     String kBaseURL = "https://demo.smartflomeet.ttns.in/"
     
 /* Your Application Credential required to try with SmartFloMeet Hosted Service
     When you setup your own Application Service, remove these */
     
     String kAppId = ""  
     String kAppkey = ""  
 ```


### 1.2 Test

#### 1.2.1 Open the App

* Open the App in your Device. You get a form to enter the credentials i.e. Name & Room Id.
* You need to create a Room by clicking the "Create Room" button.
* Once the Room Id is created, you can use it and share with others to connect to the Virtual Room to carry out an RTC Session either as a Moderator or a Participant (Choose applicable Role in the Form).

Note: Only one user with Moderator Role allowed to connect to a Virtual Room while trying with SmartFloMeet Hosted Service. Your Own Application Server may allow up to 5 Moderators.
  
 Note:- In case of emulator/simulator your local stream will not create. It will create only on real device. 
  
## 2. Set up Your Own Application Server

You may need to set up your own Application Server after you tried the Sample Application with SmartFloMeet hosted Server. We have different variants of Application Server Sample Code. Pick the one in your preferred language and follow instructions given in respective README.md file.

* NodeJS: [https://github.com/smartflomeet/Video-Conferencing-Open-Source-Web-Application-Sample.git]
* PHP: [https://github.com/smartflomeet/Group-Video-Call-Conferencing-Sample-Application-in-PHP]

Note the following:
* You need to use App ID and App Key to run this Service.
* Your Android Client End Point needs to connect to this Service to create Virtual Room and Create Token to join the session.
* Application Server is created using SmartFloMeet Server API, a Rest API Service helps in provisioning, session access and post-session reporting.  

To know more about Server API, go to:
https://doc.smartflomeet.ttns.in/developer/video-api/server-api/


## 3. Android Toolkit

This Sample Applcation uses SmartFloMeet Android Toolkit to communicate with SmartFLoMeet Servers to initiate and manage Real Time Communications. Please update your Application with latest version of SmartFloMeet Android Toolkit as and when a new release is avaialble.   

* Documentation: https://doc.smartflomeet.ttns.in/developer/video-api/server-api/
* Download Toolkit: https://doc.smartflomeet.ttns.in//developer/video-api/client-api/android-toolkit/


