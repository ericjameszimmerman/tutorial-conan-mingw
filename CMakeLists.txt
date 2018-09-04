PROJECT(MyTestingExample)
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_executable(my_test src/main.cpp src/tests/simpleTest.cpp)
target_link_libraries(my_test ${CONAN_LIBS})