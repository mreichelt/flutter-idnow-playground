# flutter_id_now

This project tries to wrap the Android and iOS SDKs of IDnow.

It's only current purpose is to debug an issue of integrating the iOS SDK.

Do not use! Yet ;)

Here's the output error when trying to run the iOS build:

```console
$ cd example
$ flutter build ios --no-codesign
Warning: Building for device with codesigning disabled. You will have to manually codesign before deploying to device.
Building com.example.flutterIdNowExample for device (ios-release)...
Warning: Missing build name (CFBundleShortVersionString).
Warning: Missing build number (CFBundleVersion).
Action Required: You must set a build name and number in the pubspec.yaml file version field before submitting to the App Store.

Running Xcode build...

Xcode build done.                                            7,0s
Failed to build iOS app
Error output from Xcode build:
↳
    ** BUILD FAILED **


Xcode's output:
↳
    /Users/mreichelt/Projects/other/flutter_id_now/ios/Classes/SwiftFlutterIdNowPlugin.swift:3:8: error: no such module 'IDnowSDK'
    import IDnowSDK
           ^
    /Users/mreichelt/Projects/other/flutter_id_now/ios/Classes/SwiftFlutterIdNowPlugin.swift:3:8: error: no such module 'IDnowSDK'
    import IDnowSDK
           ^
    note: Using new build system
    note: Planning build
    note: Constructing build description

════════════════════════════════════════════════════════════════════════════════
Building a deployable iOS app requires a selected Development Team with a
Provisioning Profile. Please ensure that a Development Team is selected by:
  1- Open the Flutter project's Xcode target with
       open ios/Runner.xcworkspace
  2- Select the 'Runner' project in the navigator then the 'Runner' target
     in the project settings
  3- In the 'General' tab, make sure a 'Development Team' is selected.
     You may need to:
         - Log in with your Apple ID in Xcode first
         - Ensure you have a valid unique Bundle ID
         - Register your device with your Apple Developer Account
         - Let Xcode automatically provision a profile for your app
  4- Build or run your project again

For more information, please visit:
  https://flutter.dev/setup/#deploy-to-ios-devices

Or run on an iOS simulator without code signing
════════════════════════════════════════════════════════════════════════════════
Encountered error while building for device.
```
