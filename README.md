# tutorial-conan-mingw
A tutorial project for using conan package manager within mingw

## Create Profile for mingw64
Create a file 'mingw64' at C:\Users\\[user]\.conan\profiles\
```
[build_requires]
[settings]
    os=Windows
    os_build=Windows
    arch=x86_64
    arch_build=x86_64
    compiler=gcc
    compiler.version=7.3
    compiler.libcxx=libstdc++
    build_type=Release
[options]
[env]
```

## Install Dependent Packages

```
 conan install --pr mingw64 --build=missing ..
```

## Build - Command Line

```
cmake .. -G "MinGW Makefiles"
make

Scanning dependencies of target my_test
[ 33%] Building CXX object CMakeFiles/my_test.dir/src/main.cpp.obj
[ 66%] Building CXX object CMakeFiles/my_test.dir/src/tests/simpleTest.cpp.obj
[100%] Linking CXX executable bin\my_test.exe
[100%] Built target my_test
```

## Output Log
```
PS D:\Projects\conan\tutorial-conan-mingw> mkdir build


    Directory: D:\Projects\conan\tutorial-conan-mingw


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----         9/3/2018  11:00 PM                build


PS D:\Projects\conan\tutorial-conan-mingw> cd .\build\
PS D:\Projects\conan\tutorial-conan-mingw\build>  conan install --pr mingw64 --build=missing ..
PROJECT: Installing D:\Projects\conan\tutorial-conan-mingw\conanfile.txt
Requirements
    gtest/1.7.0@bincrafters/stable from 'conan-center' - Cache
Packages
    gtest/1.7.0@bincrafters/stable:6ccbc70ca78a5eda2913bbdf7b358fd1786b0b27 - Build

Downloading conan_sources.tgz
[==================================================] 345B/345B
gtest/1.7.0@bincrafters/stable: Building your package in C:\Users\Eric\.conan\data\gtest\1.7.0\bincrafters\stable\build\6ccbc70ca78a5eda2913bbdf7b358fd1786b0b27
gtest/1.7.0@bincrafters/stable: Configuring sources in C:\Users\Eric\.conan\data\gtest\1.7.0\bincrafters\stable\source
[==================================================] 468.7KB/468.7KB
gtest/1.7.0@bincrafters/stable: Copying sources to build folder
gtest/1.7.0@bincrafters/stable: Generator cmake created conanbuildinfo.cmake
gtest/1.7.0@bincrafters/stable: Calling build()
-- The C compiler identification is GNU 7.3.0
-- The CXX compiler identification is GNU 7.3.0
-- Check for working C compiler: C:/Program Files/mingw-w64/x86_64-7.3.0-posix-seh-rt_v5-rev0/mingw64/bin/gcc.exe
-- Check for working C compiler: C:/Program Files/mingw-w64/x86_64-7.3.0-posix-seh-rt_v5-rev0/mingw64/bin/gcc.exe -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: C:/Program Files/mingw-w64/x86_64-7.3.0-posix-seh-rt_v5-rev0/mingw64/bin/g++.exe
-- Check for working CXX compiler: C:/Program Files/mingw-w64/x86_64-7.3.0-posix-seh-rt_v5-rev0/mingw64/bin/g++.exe -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Conan: called by CMake conan helper
-- Conan: Compiler GCC>=5, checking major version 7.3
-- Conan: Checking correct version: 7.3
-- Conan: Using cmake global configuration
-- Conan: Adjusting default RPATHs Conan policies
-- Conan: Adjusting language standard
-- Conan: C++ stdlib: libstdc++
-- Found PythonInterp: C:/Program Files/Python37/python.exe (found version "3.7")
-- Looking for pthread.h
-- Looking for pthread.h - found
-- Looking for pthread_create
-- Looking for pthread_create - found
-- Found Threads: TRUE
-- Configuring done
-- Generating done
CMake Warning:
  Manually-specified variables were not used by the project:

    CMAKE_EXPORT_NO_PACKAGE_REGISTRY


-- Build files have been written to: C:/Users/Eric/.conan/data/gtest/1.7.0/bincrafters/stable/build/6ccbc70ca78a5eda2913bbdf7b358fd1786b0b27
Scanning dependencies of target gtest
[ 25%] Building CXX object source_subfolder/CMakeFiles/gtest.dir/src/gtest-all.cc.obj
In file included from C:\Users\Eric\.conan\data\gtest\1.7.0\bincrafters\stable\build\6ccbc70ca78a5eda2913bbdf7b358fd1786b0b27\source_subfolder\src\gtest-all.cc:43:0:
C:/Users/Eric/.conan/data/gtest/1.7.0/bincrafters/stable/build/6ccbc70ca78a5eda2913bbdf7b358fd1786b0b27/source_subfolder/src/gtest-death-test.cc:123:13: warning: 'testing::internal::g_in_fast_death_test_child' defined but not used [-Wunused-variable]
 static bool g_in_fast_death_test_child = false;
             ^~~~~~~~~~~~~~~~~~~~~~~~~~
[ 50%] Linking CXX shared library ..\bin\libgtest.dll
[ 50%] Built target gtest
Scanning dependencies of target gtest_main
[ 75%] Building CXX object source_subfolder/CMakeFiles/gtest_main.dir/src/gtest_main.cc.obj
[100%] Linking CXX shared library ..\bin\libgtest_main.dll
[100%] Built target gtest_main
gtest/1.7.0@bincrafters/stable: Package '6ccbc70ca78a5eda2913bbdf7b358fd1786b0b27' built
gtest/1.7.0@bincrafters/stable: Build folder C:\Users\Eric\.conan\data\gtest\1.7.0\bincrafters\stable\build\6ccbc70ca78a5eda2913bbdf7b358fd1786b0b27
gtest/1.7.0@bincrafters/stable: Generated conaninfo.txt
gtest/1.7.0@bincrafters/stable: Generated conanbuildinfo.txt
gtest/1.7.0@bincrafters/stable: Generating the package
gtest/1.7.0@bincrafters/stable: Package folder C:\Users\Eric\.conan\data\gtest\1.7.0\bincrafters\stable\package\6ccbc70ca78a5eda2913bbdf7b358fd1786b0b27
gtest/1.7.0@bincrafters/stable: Calling package()
gtest/1.7.0@bincrafters/stable package(): Copied 1 file: LICENSE
gtest/1.7.0@bincrafters/stable package(): Copied 20 '.h' files:
gtest/1.7.0@bincrafters/stable package(): Copied 4 '.a' files: libgtest.dll.a, libgtest_main.dll.a, objects.a, objects.a
gtest/1.7.0@bincrafters/stable package(): Copied 2 '.dll' files: libgtest.dll, libgtest_main.dll
gtest/1.7.0@bincrafters/stable: Package '6ccbc70ca78a5eda2913bbdf7b358fd1786b0b27' created
PROJECT: Generator cmake created conanbuildinfo.cmake
PROJECT: Generator txt created conanbuildinfo.txt
PROJECT: Generated conaninfo.txt
PS D:\Projects\conan\tutorial-conan-mingw\build> cmake .. -G "MinGW Makefiles"
-- The C compiler identification is GNU 7.3.0
-- The CXX compiler identification is GNU 7.3.0
-- Check for working C compiler: C:/Program Files/mingw-w64/x86_64-7.3.0-posix-seh-rt_v5-rev0/mingw64/bin/gcc.exe
-- Check for working C compiler: C:/Program Files/mingw-w64/x86_64-7.3.0-posix-seh-rt_v5-rev0/mingw64/bin/gcc.exe -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: C:/Program Files/mingw-w64/x86_64-7.3.0-posix-seh-rt_v5-rev0/mingw64/bin/g++.exe
-- Check for working CXX compiler: C:/Program Files/mingw-w64/x86_64-7.3.0-posix-seh-rt_v5-rev0/mingw64/bin/g++.exe -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Current conanbuildinfo.cmake directory: D:/Projects/conan/tutorial-conan-mingw/build
-- Conan: Compiler GCC>=5, checking major version 7.3
-- Conan: Checking correct version: 7.3
-- Conan: Using cmake global configuration
-- Conan: Adjusting default RPATHs Conan policies
-- Conan: Adjusting language standard
-- Configuring done
-- Generating done
-- Build files have been written to: D:/Projects/conan/tutorial-conan-mingw/build
PS D:\Projects\conan\tutorial-conan-mingw\build>
```