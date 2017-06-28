# Install OpenCV and OpenCV-text module with Visual Studio 2017 on Win10

It's complicated. First tried with cmake and stuff, but got dependency problems,
particularly with Tesseract integration with OpenCV.

Then stumbled across CPPAN. 

# Instructions
1. Install CPPAN. Remember to put cppan.exe somewhere in the PATH.
   https://cppan.org/
   
2. Install CMake for Windows.
   https://cmake.org/download/

3. Install Tesseract OCR binaries for Windows
   https://github.com/tesseract-ocr/tesseract/wiki/4.0-with-LSTM#400-alpha-for-windows
   Remember to set TESSDATA_PREFIX to C:\Program Files (x86)\Tesseract-OCR\tessdata
   
4. Install Visual Studio 2017 Community Edition (free one)
   - in the installer enable 
      * Visual Studio C++ core features
	  * VC++ 2017 v141 toolset(x86,64)
	  * Windows 10 SDK for Desktop
	  * Visual C++ tools for CMake
	  
5. Run build.bat from Visual 2017 Developer command prompt. 
6. The libraries in this repo are built for Release x86 configuration using instruction 1-5 above.
7. Include directories are also provided for opencv and opencv-contrib(text module).  
8. Add the bin directory in this repo to the PATH.


