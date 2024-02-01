# impeller_bug

### Steps to reproduce

1. Clone the sample repo (https://github.com/MillerAdulu/sturdy-robot)
2. Run on Android

### Expected results

The UI should look the same on both Android and iOS

### Actual results

When I run this project and set up an SVG as an Icon, using the colour filter from the SVG package

```
dart
colorFilter: const ColorFilter.mode(
  Colors.green,
  BlendMode.color, // Colors the entire screen green on Android instead of just the Icon
  // BlendMode.srcIn, // Works well
),
```

the entire page is coloured green on Android instead of just the SVG icon. 


### Code sample

<details open><summary>Code sample</summary>
https://github.com/MillerAdulu/sturdy-robot


</details>


### Screenshots or Video

<details open>
<summary>Screenshots / Video demonstration</summary>

![android](https://github.com/flutter/flutter/assets/21357409/eb86a39b-d08f-4e7c-a230-f77b57ab60f2)
![ios](https://github.com/flutter/flutter/assets/21357409/dc5cc4b3-bb70-42c4-b941-e0a9cc80a423)

</details>


### Logs

<details open><summary>Logs</summary>

```console
Android
Launching lib/main.dart on Nokia C21 Plus in debug mode...
Running Gradle task 'assembleDebug'...                             85.6s
✓  Built build/app/outputs/flutter-apk/app-debug.apk.
Installing build/app/outputs/flutter-apk/app-debug.apk...           6.7s
Syncing files to device Nokia C21 Plus...                          325ms

Flutter run key commands.
r Hot reload. 🔥🔥🔥
R Hot restart.
h List all available interactive commands.
d Detach (terminate "flutter run" but leave application running).
c Clear the screen
q Quit (terminate the application on the device).

A Dart VM Service on Nokia C21 Plus is available at: http://127.0.0.1:49215/3kPew2ALLE4=/
The Flutter DevTools debugger and profiler on Nokia C21 Plus is available at:
http://127.0.0.1:9101?uri=http://127.0.0.1:49215/3kPew2ALLE4=/
D/IMGGralloc(25668): Gralloc Register  w:720, h:1600, f:0x1, usage:0xb00, ui64Stamp:3804611, sSize:4608000, line = 2335

Performing hot reload...                                                
Reloaded 1 of 939 libraries in 2,108ms (compile: 195 ms, reload: 784 ms, reassemble: 864 ms).
D/IMGGralloc(25668): Gralloc Register  w:720, h:1572, f:0x1, usage:0xb00, ui64Stamp:3804659, sSize:4562944, line = 2335

Performing hot reload...                                                
Reloaded 1 of 939 libraries in 1,506ms (compile: 72 ms, reload: 719 ms, reassemble: 659 ms).

Performing hot reload...                                                
Reloaded 1 of 939 libraries in 1,725ms (compile: 81 ms, reload: 727 ms, reassemble: 866 ms).

Performing hot reload...                                                
Reloaded 1 of 939 libraries in 1,635ms (compile: 56 ms, reload: 806 ms, reassemble: 731 ms).

Performing hot reload...                                                
Reloaded 1 of 939 libraries in 1,496ms (compile: 59 ms, reload: 732 ms, reassemble: 662 ms).

Performing hot reload...                                                
Reloaded 1 of 939 libraries in 1,463ms (compile: 31 ms, reload: 736 ms, reassemble: 657 ms).

Performing hot reload...                                                
Reloaded 1 of 939 libraries in 1,497ms (compile: 61 ms, reload: 736 ms, reassemble: 654 ms).

Performing hot reload...                                                
Reloaded 1 of 939 libraries in 1,512ms (compile: 79 ms, reload: 737 ms, reassemble: 648 ms).
D/IMGGralloc(25668): Gralloc Free  w:720, h:1572, f:0x1, usage:0xb00, ui64Stamp:3804543 line = 2441
D/IMGGralloc(25668): Gralloc Free  w:720, h:1572, f:0x1, usage:0xb00, ui64Stamp:3804659 line = 2441
E/OpenGLRenderer(25668): reset ##### pid = 25724
D/IMGGralloc(25668): Gralloc Free  w:720, h:1600, f:0x1, usage:0xb00, ui64Stamp:3804611 line = 2441
Application finished.


iOS
Launching lib/main.dart on iPhone 15 Pro Max in debug mode...
Running Xcode build...                                               
 └─Compiling, linking and signing...                        24.6s
Xcode build done.                                           91.1s
[ERROR:flutter/shell/platform/darwin/graphics/FlutterDarwinContextMetalImpeller.mm(42)] Using the Impeller rendering backend.
Syncing files to device iPhone 15 Pro Max...                     1,897ms

Flutter run key commands.
r Hot reload. 🔥🔥🔥
R Hot restart.
h List all available interactive commands.
d Detach (terminate "flutter run" but leave application running).
c Clear the screen
q Quit (terminate the application on the device).

A Dart VM Service on iPhone 15 Pro Max is available at: http://127.0.0.1:49925/NY7ONtOsCBo=/
The Flutter DevTools debugger and profiler on iPhone 15 Pro Max is available at:
http://127.0.0.1:9101?uri=http://127.0.0.1:49925/NY7ONtOsCBo=/
```

</details>


### Flutter Doctor output

<details open><summary>Doctor output</summary>

```console
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.16.4, on macOS 14.2.1 23C71 darwin-arm64, locale en-KE)
[✓] Android toolchain - develop for Android devices (Android SDK version 34.0.0)
[✓] Xcode - develop for iOS and macOS (Xcode 15.2)
[✓] Chrome - develop for the web
[✓] Android Studio (version 2023.1)
[✓] VS Code (version 1.85.2)
[✓] Connected device (2 available)
[✓] Network resources

• No issues found!
```

</details>
