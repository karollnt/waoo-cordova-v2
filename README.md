# waoo-cordova

## Building for Android

### For Testing in Device

```
cordova build android
cordova run android
```

### For Release
```
cordova build --release
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore release-key.keystore platforms/android/build/outputs/apk/android-release-unsigned.apk waoo
zipalign -v 4 platforms/android/build/outputs/apk/android-release-unsigned.apk android-release.apk
```

## Building for iOS

### For Testing in Device

```
cordova build ios
cordova run ios
```

### For Release

Open Workspace in XCode

```
open platforms/ios/Waoo.xcworkspace
```
