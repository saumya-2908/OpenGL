**Android OpenCV Camera --**
=========================================

This project demonstrates how to integrate **OpenCV** with an **Android Camera** pipeline to process real-time frames using native C++ code through the Android NDK. It provides a simple, extendable template for computer-vision tasks such as object detection, edge processing, filtering, and OpenGL rendering.

* * * * *

🚀 **Features**
---------------

-   Live camera preview using Android Camera API

-   OpenCV integration for real-time image processing

-   Native C++ (NDK) pipeline for improved performance

-   Custom GLSurfaceView renderer for displaying processed frames

-   Modular structure for adding your own OpenCV algorithms

-   Clean and renamed package structure (no third-party author references)

* * * * *

🧱 **Project Structure**
------------------------

`app/
 ├── src/
 │    ├── main/
 │    │    ├── java/.../camera/     # Camera activity, GLSurfaceView, rendering
 │    │    ├── cpp/                 # Native C++ OpenCV code
 │    │    ├── res/                 # Layouts & UI resources
 │    │    └── AndroidManifest.xml
 ├── CMakeLists.txt                 # C++/NDK build config
 ├── build.gradle                   # App-level Gradle config
OpenCV/                              # (If included) OpenCV SDK module
README.md                            # This file`

* * * * *

📦 **Requirements**
-------------------

-   **Android Studio (latest recommended)**

-   **OpenCV for Android SDK**

-   **Android NDK**

-   Minimum Android API level: **21** (modifiable)

* * * * *

🛠️ **How to Build**
--------------------

1.  Download and install **OpenCV for Android**

2.  Copy the `OpenCV-android-sdk/sdk/native/libs` folder into your project (if not already included)

3.  Make sure the path in `CMakeLists.txt` points to your OpenCV native libs

4.  Open the project in Android Studio

5.  Let Gradle sync & press **Run**

* * * * *

🖥️ **How It Works**
--------------------

-   The camera preview frames are captured in Java/Kotlin.

-   Frames are sent to **native-lib.cpp**, where OpenCV processes them.

-   Processed frames are passed to the **GLSurfaceView** renderer.

-   The result is drawn onto the screen in real time.

This architecture makes it easy to replace the default processing with your own OpenCV code such as:

`cv::cvtColor(inputFrame, outputFrame, cv::COLOR_RGBA2GRAY);
cv::GaussianBlur(outputFrame, outputFrame, cv::Size(5, 5), 0);`

* * * * *

✨ **Customization**
-------------------

You can easily add:

-   Face detection

-   Object tracking

-   Edge or contour processing

-   Color filters

-   AR overlays

-   Custom shaders
