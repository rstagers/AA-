Versions of the AA+ library code.  

Unzip the code into the directory with the version number.

Then from the terminal run cmake-gui, set the paths to the
source ans specify a build directory under that.  Then press Configure
and select if you want a debug library of not.  I set DEBUG so the lib is a 
debug version.  The code needs to stay in place so it can be found.  (I think).

Then run generate, this will create the Makefile to build the library and test
code.  Change to the build directo and make...

To update the shared library...
copy the new version to /use/local/lib (needs sudo)
then run: sudo ldconfig

Remember that any project in Eclipse using the library will need to change where the 
include directory is so it will match the library in use.  Shouldn't matter for the 
most part but to be correct that is what we should do unless I implement versioned
libraries.

