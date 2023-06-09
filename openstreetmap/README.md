# openstreetmap

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

## Screenshot

![Screenshot](./Screenshot.png)

## Installing

- [flutter_map](https://github.com/fleaflet/flutter_map)  
  A wrapper around InheritedWidget to make them easier to use and more reusable.

  ```shell
  fvm flutter pub add flutter_map
  fvm flutter pub add latlong2
  ```

  Import it

  ```dart
  import 'package:flutter_map/flutter_map.dart';
  ```

## Configure

Edit `android/app/src/main/AndroidMainfest.xml`

```xml
<manifest ... >
    <uses-permission android:name="android.permission.INTERNET"/>
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
    <uses-permission android:name="android.permission.ACCESS_BACKGROUND_LOCATION" />
    ...
</manifest>
```

```xml
<manifest ... >
    <application ...
        android:usesCleartextTraffic="true">
        ...
    </application>
</manifest>
```

Edit `ios/Runner/info.plist`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<plist version="1.0">
<dict>
    ...
    <key>NSLocationWhenInUseUsageDescription</key>
    <string>This app needs access to location when open.</string>
    <key>NSLocationAlwaysUsageDescription</key>
    <string>This app needs access to location when in the background.</string>
</dict>
</plist>
```

```xml
<?xml version="1.0" encoding="UTF-8"?>
<plist version="1.0">
<dict>
    ...
    <key>NSAppTransportSecurity</key>
    <dict>
        <key>NSAllowsLocalNetworking</key>
        <true/>
        <key>NSAllowsArbitraryLoadsInWebContent</key>
        <true/>
    </dict>
</dict>
</plist>
```
