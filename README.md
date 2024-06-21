## A template project using cmake and WIX

This is a simple template for building Windows installers
using cmake and wix

Suggested use:
```
mkdir build
cmake --build build --config Release # builds the .exe
cd build
cpack -G WIX # builds the .msi
```
