# Flying-Cows

UAlberta Multimedia Program MM802 Course Project: Real-Time cow counting from video or image stack captured from a drone

Codes of the project will be uploaded once this semester would be ended. 

## Get Started

### Package Installation with CocoaPods

Since this project has been integrated with CocoaPods now, please check the following steps to install all the packages using CocoaPods after you downloading this project:

**1.** Install CocoaPods

Open Terminal and change to the download project's directory, enter the following command to install it:

~~~
sudo gem install cocoapods
~~~

The process may take a long time, please wait. For further installation instructions, please check [this guide](https://guides.cocoapods.org/using/getting-started.html#getting-started).

**2.** Install SDK and DJIWidget with CocoaPods in the Project

Run the following command in the **SwiftSampleCode** paths:

~~~
pod install
~~~

If you install it successfully, you should get the messages similar to the following:

~~~
Analyzing dependencies
Downloading dependencies
Installing DJI-SDK-iOS (4.14)
Installing DJIWidget (1.6.4)
Installing DJIFlySafeDatabaseResource (01.00.01.18)
Installing ICycleView (1.0.0)
Installing SwiftHTTP (3.0.1)
Installing SwiftyJSON (4.0)
Generating Pods project
Integrating client project

[!] Please close any current Xcode sessions and use `DJISdkDemo.xcworkspace` for this project from now on.
Pod installation complete! There is 1 dependency from the Podfile and 1 total pod
installed.
~~~

> **Note**: If you saw "Unable to satisfy the following requirements" issue during pod install, please run the following commands to update your pod repo and install the pod again:
> 
> ~~~
> pod repo update
> pod install
> ~~~
> 


### Run Sample Code

Since this project is built on DJI SDK, you will need to setup the App Key by editing the sample code's info.plist, [after generating their unique App Key](https://developer.dji.com/mobile-sdk/documentation/quick-start/index.html#generate-an-app-key).

The DJISDKAppKey is present in the Info.plist - you just need to add their unique key.
You will still need to update the [Bundle Identifier](http://developer.dji.com/user/mobile-sdk/ios-configuration/) .

One of DJI's aircraft or handheld cameras will be required to run this application.  


## What this app can do?

1. Image transmission via HTTP POST using Base64 encoding.
2. Receive HTTP Response and decode the imageData back to UIImage for display.
3. Create waypoint missions for the drone.
4. View basic information of the drone.
