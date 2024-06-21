## A template project using cmake and WIX

This is a simple template for building Windows installers
using cmake and wix

Suggested use:
```
mkdir build
cd build
cmake ..
cmake --build . --config Release # builds the .exe
cpack -G WIX # builds the .msi
cd ..
```
