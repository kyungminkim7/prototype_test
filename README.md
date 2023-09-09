## Overview
This repo provides a ready-made project structure for quick testing/prototyping using Googletest.

## Dependencies
- CMake >= 3.20
- C++17 Compiler

## Initial Build/Test Instructions
1. Add tests to `prototype_test.cpp`
2. Generate build system (run from project root directory):
```
cmake -B build -S .
```
3. Navigate to generated `build` directory
```
cd build
```
4. Build and test:
```
cmake --build . && ctest -VV --stop-on-failure
```

## Subsequent Build/Test Instructions
1. Add tests to `prototype_test.cpp`
2. Build and test (run from `build` directory):
```
cmake --build . && ctest -VV --stop-on-failure
```