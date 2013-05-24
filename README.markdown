# Description

Apple stopped supporting a unique identifier for iOS. This source code solves the problem. It generates a unique identifier based on the mac address of the device in combination with the bundle identifier.

What you need to do:

- copy `NSString+MD5Addition` and `UIDevice+IdentifierAddition` to your project.

- if your are using ARC in your project, you have to add the `-fno-objc-arc` flag to both files. [Apple ARC Guidelines](http://developer.apple.com/library/mac/#releasenotes/ObjectiveC/RN-TransitioningToARC/Introduction/Introduction.html)

- use `[[UIDevice currentDevice] uniqueDeviceIdentifier]` to retrieve the unique identifier (it's a hash of your Bundle ID + MAC address)

- use `[[UIDevice currentDevice] uniqueGlobalDeviceIdentifier]` to retrieve a global unique identifier (it's a hash of the MAC address, used for tracking between different apps).

- have fun and follow [gekitz](http://twitter.com/gekitz) ;)

//Thanks to Erica Sadun for her UIDevice+Hardware Addition (used for the mac address retrieval).

<!-- MacBuildServer Install Button -->
<div class="macbuildserver-block">
    <a class="macbuildserver-button" href="http://macbuildserver.com/project/github/build/?xcode_project=UIDeviceAddition.xcodeproj&amp;target=UIDeviceAddition&amp;repo_url=git%3A%2F%2Fgithub.com%2Fgekitz%2FUIDevice-with-UniqueIdentifier-for-iOS-5.git&amp;build_conf=Release" target="_blank"><img src="http://com.macbuildserver.github.s3-website-us-east-1.amazonaws.com/button_up.png"/></a><br/><sup><a href="http://macbuildserver.com/github/opensource/" target="_blank">by MacBuildServer</a></sup>
</div>
<!-- MacBuildServer Install Button -->

# License
see license file.

