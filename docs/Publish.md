## Step 5: Publish

In your project's `platforms` directory, you have two complete native projects: one for Android, and one for iOS. You can build release versions of these projects and publish them to Google Play or to the iOS App Store.

### Publish to the Play Store

To publish your Android application to the Play Store:

1. Edit `platforms/android/AndroidManifest.xml` and set the `versionCode` and `versionName` properties correctly.

2. Edit (or create) `platforms/android/ant.properties` and set the `key.store` and `key.alias` properties (as explained [in the Android developer docs](http://developer.android.com/tools/building/building-cmdline.html#ReleaseMode)).

3. Build your project:

        ./platforms/android/cordova/build --release

4. Find your signed .apk located in `platforms/android/ant-build`.

5. Upload your signed application to the Google Play developer console.

### Publish to the iOS App Store

Open the Xcode project file found under your `platforms/ios` directory:

    open platforms/ios/*.xcodeproj
    
And then follow Apple's [App Distribution Guide](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/Introduction/Introduction.html)
