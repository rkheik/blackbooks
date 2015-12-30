# iOS Resources

## References
* General
  * [AppStore iOS fragmentation](https://developer.apple.com/support/app-store/)
  * [App review times](http://appreviewtimes.com/)
* Hardware
  * [iOS support matrix](http://iossupportmatrix.com/)
  * [UDID (for clients)](http://whatsmyudid.com/)
  * [UDID (for clients) no iTunes](http://get.udid.io)
* UI
  * [iOS HIG](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/)
  * [watch HIG](https://developer.apple.com/watch/human-interface-guidelines/)
  * [iphoneresolution](http://www.iphoneresolution.com)
  * [iphoneresolution guide](http://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions)
  * [iOSRes](http://iosres.com)
* Code
  * [App programming guide](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072-CH1-SW1)
  * [64-bit requirements](https://developer.apple.com/news/?id=04082015a)
  * [Cocoa touch 64-bit](https://developer.apple.com/library/ios/documentation/General/Conceptual/CocoaTouch64BitGuide/Introduction/Introduction.html)
  * [App Extension Programming Guide](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/)
* Documentations
  * [Headerdoc (obj-c)](https://developer.apple.com/library/mac/documentation/DeveloperTools/Conceptual/HeaderDoc/intro/intro.html)
  * [Appledoc (obj-c)](https://github.com/tomaz/appledoc)
  * [reStructuredText (swift)](http://docutils.sourceforge.net/docs/user/rst/quickref.html)
* Style guides
  * [Github obj-c](https://github.com/github/objective-c-style-guide)
  * [raywenderlich obj-c](https://github.com/raywenderlich/swift-style-guide)
  * [raywenderlich swift](https://github.com/raywenderlich/objective-c-style-guide)
* Dependency managers
  * [Cocoapods](https://github.com/CocoaPods/CocoaPods)
  * [Carthage](https://github.com/Carthage/Carthage)
  * Swift only in iOS8(Dynamic frameworks)
  * [CocoaSeeds(swift ios7)](https://github.com/devxoul/CocoaSeeds)
* Xcode plugins
  * [Alcatraz](http://alcatraz.io/)
* Distribution
  * [App distribution guide](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/Introduction/Introduction.html)
  * [Itunes connect developer guide](https://developer.apple.com/library/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Chapters/About.html#//apple_ref/doc/uid/TP40011225-CH1-SW1)
  * [Appstore guidelines](https://developer.apple.com/app-store/review/guidelines/)
* Beta testing
  * [Fabric.io](https://get.fabric.io)
  * [Hockeyapp](http://hockeyapp.net)
  * [Testfairy](http://www.testfairy.com)
  * [Installr](https://www.installrapp.com/)
  * [Diawi](http://www.diawi.com/)
  * [testflight alternatives](https://www.playtestcloud.com/blog/testflight-alternatives-ios-android)
* Libs
  * DB
    * [FMDB](https://github.com/ccgus/fmdb)
  * Net
    * [AFNetworking](https://github.com/AFNetworking/AFNetworking)
    * [Alamofire](https://github.com/Alamofire/Alamofire)
  * Other
    * [Then(syntactic sugar initializers)](https://github.com/devxoul/Then)

## Quick tables

### iOS versions

|date              |WWDC|iOS|Final|
|------------------|----|---|-----|
|     June 21, 2010|-   |4  |4.3.4|
|  October 12, 2011|2011|5  |5.1.1|
|September 19, 2012|2012|6  |6.1.6|
|September 18, 2013|2013|7  |7.1.2|
|September 17, 2014|2014|8  |8.4.1(?)|
|September 16, 2015|2015|9  |-    |

### XCode - SDKs
[What’s New in Xcode](https://developer.apple.com/library/prerelease/ios/documentation/DeveloperTools/Conceptual/WhatsNewXcode/Articles/xcode_7_0.html)

|Major|Minor|Features|iOS SDK    |OSX   |
|-----|-----|--------|-----------|------|
|4    |4.1  |         |          |10.7  |
|4    |4.2  |         |5.0       |10.7  |
|4    |4.3.1|         |5.1       |10.7  |
|4    |4.4  |         |5.1       |10.8  |
|4    |4.5  |         |6.0       |10.8  |
|4    |4.6  |         |6.1       |10.8  |
|4    |4.6.1|         |6.1       |10.8.3|
|5    |5.0  |         |7.0       |10.8  |
|5    |5.0.1|         |7.0       |10.9  |
|5    |5.1  |         |7.1       |10.9  |
|6    |6.0  |swift 1.0|8.0       |10.9  |
|6    |6.1  |swift 1.1|8.0       |10.10 |
|6    |6.2  |watchkit |8.2       |10.10 |
|6    |6.3  |swift 1.2|8.3       |10.10 |
|6    |6.4  |         |8.4       |10.10 |
|7    |7.0  |watchOS2, swift2.0|9.0       |10.11 |
|7    |7.1  |tvOS     |9.1       |10.11 |
|7    |7.2  |watchOS2.1|9.2       |10.11 |

[Swift OSS!](https://swift.org/)

### OSX Versions
|Version|Name         |
|-------|-------------|
|10.5   |Leopard      |
|10.6   |Snow Leopard |
|10.7   |Lion         |
|10.8   |Mountain Lion|
|10.9   |Mavericks    |
|10.10  |Yosemite     |
|10.11  |El Capitan   |

### Resolutions

|Device           |Retina|Resolution|
|-----------------|------|----------|
|1st Gen, 3G & 3GS|1x    |320×480   |
|4 & 4S           |2x    |640×960   |
|5, 5C & 5S       |2x    |640×1136  |
|6, 6s            |2x    |750×1334  |
|6+, 6s+          |3x    |1242×2208 (1080×1920)|
|Apple watch 38mm |-     |272x340   |
|Apple watch 42mm |-     |312x390   |


### Frameworks
[iOS Frameworks](https://developer.apple.com/library/ios/documentation/Miscellaneous/Conceptual/iPhoneOSTechOverview/iPhoneOSFrameworks/iPhoneOSFrameworks.html)

|First avaliable iOS|Frameworks     |
|:-----------------:|:-------------:|
|4|Accelerate, AssetsLibrary, CoreMedia, CoreMotio, CoreTelephony, CoreVideo, EventKi, EventKitU, iAd, ImageIO, QuickLook|
|4.2|CoreMIDI|
|5|Accounts, CoreBluetooth, CoreImage, GLKit, GSS, NewsstandKit, Twitter|
|6|AdSupport, MediaToolbox, PassKit, Social, VideoToolbox|
|7|GameController, JavaScriptCore, MediaAccessibility, MultipeerConnectivity, SafariServices, SpriteKit|
|8|AVKit, CloudKit, CoreAudioKit, HealthKit, HomeKit, LocalAuthentication, Metal, NetworkExtension, NotificationCenter, Photos, PhotosUI, PushKit, SceneKit, WebKit|
|9| update*|


### Major changes
[What's New in iOS](https://developer.apple.com/library/ios/releasenotes/General/WhatsNewIniOS/Articles/iOS9_1.html)

* iOS 5
  * Siri
  * iCloud APIs
  * ARC
  * Storyboards
  * Newstand
  * Frameworks
    * GLKit
    * CoreImage
    * Twitter
    * Accounts
    * CoreBluetooth
  * UIAppearance
  * ContainerView

* iOS 6
  * Apple maps
  * PassKit
  * Reminders
  * In-App purchase
  * CollectionViews
  * Autolayout
  * UI State restoration
  * Attributed strings
  * UIRefreshcontrol

* iOS 7
  * New UI
  * CarPlay
  * Dynamic behaviors for views
  * 64-bit
  * New background modes(content in back, push notifs)
  * Frameworks
    * SpriteKit
    * GameController
    * Multipeer
  * UIMotionEffect
  * Dynamic text sizing
  * OpenGL ES 3.0
  * Get mac address deprecated

* iOS 8
  * App extensions(share, action, keyboards, watchapp)
  * TouchID
  * Size classes
    * backwards compatibe if the value of the height component is not compact
  * Adaptive segues
    * versions below iOS 8.0, adaptive segues are converted to legacy segues
  * Location Manager
    * whenInUseUsage, alwaysUsage
  * Handoff
  * Apple watch(8.2)
  * ApplePay(8.1)
  * iCloud drive
  * Frameworks
    * Metal
    * SceneKit
    * HealthKit
    * HomeKit
    * CloudKit
    * WatchKit
  * UISplitViewController on iphones
  * UIAlertController

* iOS 9
  * Multitask iPad(slide over, split view, PiP)
  * 3D Touch
  * Inside app search
  * AppThining
  * App Transport Security
  * New extension points(network, safari, reindexing, etc)
  * Frameworks
    * WatchConnectivity
    * Contacts & ContactsUI
  * Maps ETA/Transit
  * Passbook -> Wallet
  * UIStackView
