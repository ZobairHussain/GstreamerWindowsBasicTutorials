# Install GStreamer on Windows
### A guide by Zobair

Official documentation
Gstreamer installation official  guide is too old and is not updated properly with current technologies.
Official doc: https://gstreamer.freedesktop.org/documentation/installing/on-windows.html?gi-language=c


1. Download
Download both runtime installer & development installer from MSVC 64-bit from below link
https://gstreamer.freedesktop.org/download/#windows

2. Add Environment Variable to system
Add your installed location to ENV variable.
Variable name: GSTREAMER_1_0_ROOT_MSVC_X86_64
Variable value: C:\gstreamer\1.0\msvc_x86_64
Note: Your variable value could be different.

3. Add Environment Variable Path
Add %GSTREAMER_1_0_ROOT_MSVC_X86_64%\bin to environment variable path 
Then restart PC

4. Check  Environment Variable Path
Check if your variable path is added successfully

5. Create New Project
Create new Visual Studio C++ Console App named basic-tutorial-1

6. Run Hello World
Check if your hello world project is running successfully

7. Basic Tutorial 1
Copy basic-tutorial-1.c full code from here and paste to your project 
https://gstreamer.freedesktop.org/documentation/tutorials/basic/hello-world.html?gi-language=c

8. Add properties
Go to Property Manager and add E:\gstreamer\1.0\msvc_x86_64\share\vs\2010\libs\gstreamer-1.0.props to existing property sheet 

9. Fix error
Error: argument of type "int" is incompatible with parameter of type "GstMessageType"
Fix: Try replacing GST_MESSAGE_ERROR | GST_MESSAGE_EOS with (GstMessageType)(GST_MESSAGE_ERROR | GST_MESSAGE_EOS)

10. Run the project
Run the project.
It will play a video from net.
Noe: Only first 4 tutorial will be build by this way.

For detail guide please follow this https://github.com/ZobairHussain/GstreamerWindowsBasicTutorials/blob/master/Install%20GStreamer%20on%20Windows.pdf
