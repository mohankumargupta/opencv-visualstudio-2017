# Install OpenCV and OpenCV-text module with Visual Studio 2017 on Win10

It's complicated. First tried with cmake and stuff, but got dependency problems,
particularly with Tesseract integration with OpenCV.

Then stumbled across CPPAN. 

# Instructions

These are the steps I took to build opencv, opencv-contrib and dependencies. 
You can skip steps 1,2,5 by simple downloading and unzip this repo to somewhere on your computer.

1. Install CPPAN. Remember to put cppan.exe somewhere in the PATH.
   https://cppan.org/
   
2. Install CMake for Windows.
   https://cmake.org/download/

3. Install Tesseract OCR binaries for Windows
   https://github.com/tesseract-ocr/tesseract/wiki/4.0-with-LSTM#400-alpha-for-windows
   Remember to set environment variable TESSDATA_PREFIX to C:\Program Files (x86)\Tesseract-OCR\tessdata
      
4. Install Visual Studio 2017 Community Edition (free one)
   - in the installer enable 
      * Visual Studio C++ core features
	  * VC++ 2017 v141 toolset(x86,64)
	  * Windows 10 SDK for Desktop
	  * Visual C++ tools for CMake
	  
5. Run build.bat from Visual 2017 Developer command prompt. 


6. The libraries in this repo are built for Release x86 configuration using instruction 1-5 above. 
7. Include directories are also provided for opencv and opencv-contrib(text module).  
   In VS2017, Project->[name-of-project] Properties->C++->General->Additional Include Directories
8. Add the bin directory in this repo to the PATH. Also add to Project->[name-of-project] Properties->Linker->General->Additional Library Dependencies
9. Finally, add the following to Project->[name-of-project] Properties->Linker->Input

pvt.cppan.demo.intel.opencv.core-3.2.0.lib
pvt.cppan.demo.intel.opencv.highgui-3.2.0.lib
pvt.cppan.demo.intel.opencv.imgproc-3.2.0.lib
pvt.cppan.demo.intel.opencv.imgcodecs-3.2.0.lib
pvt.cppan.demo.intel.opencv.contrib.text-3.2.0.lib
pvt.cppan.demo.intel.opencv.videoio-3.2.0.lib

10. An example VS2017 solution file is available in this repo under the opencv-cppan folder.





