
At a console:

```
git clone --recursive https://github.com/coolprop/coolprop_fortran
cd coolprop_fortan
mkdir build
cd build
cmake .. -G "MinGW Makefiles" -DCMAKE_BUILD_TYPE=Release
cmake --build .
```