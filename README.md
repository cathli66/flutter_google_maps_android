# Google Maps in Flutter - Android App

This Flutter demo displays a simple Google Map using Google Map's Android SDK.
Does not include an API key - generate your own following the instructions here: https://developers.google.com/maps/documentation/android-sdk/get-api-key

You will need to create a Google Cloud account and add your billing information. For demo or any personal use purposes, the credits that Google provides should cover any costs.
There are multiple ways to configure the API key, but the easiest is to set Application restrictions to None and API restrictions to Maps SDK for Android (and as many others as you need). If you want to set the Application restriction to Android apps, this is more secure but you'll have to provide your app's package name and SHA fingerprint to the Google Cloud Console. These should appear if you try to run the app with the Android Application restriction active.

Then go to android/app/src/main/AndroidManifest.xml and replace YOUR_API_KEY with the API key.
<meta-data android:name="com.google.android.geo.API_KEY"
               android:value="YOUR_API_KEY"/>

To run the app, open up a terminal and use the flutter command line tool.
$ flutter run

## Getting Started with Flutter

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

## Basic tutorial on integrating Google Maps to Flutter

Includes information on setting up Flutter environment and Android emulators in Android Studio.
https://codelabs.developers.google.com/codelabs/google-maps-in-flutter#0

Make sure you also enable Google Play Services in your Android Studio's SDK Tools!
In Android Studio: Tools (Windows) or Preferences (Mac) -> SDK Manager -> SDK Tools -> check Google Play services -> Apply (downloads or updates the services)

Your Android emulator may also need to support the Google Play store. When creating your emulator, look for a version with the play icon.

## Other References

Google Maps in Flutter Android Example
Referenced code to detect and use latest renderer. Solely following the tutorial did not work, likely due to issues with the legacy renderer.
https://github.com/flutter/packages/blob/main/packages/google_maps_flutter/google_maps_flutter_android/example/lib/main.dart

Documentation on the Android SDK's new map renderer:
https://pub.dev/packages/google_maps_flutter_android#map-renderer
https://developers.google.com/maps/documentation/android-sdk/renderer
