cmake_minimum_required(VERSION 3.25.0)
project(WinCppTemplate VERSION 1.0)

# specify the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

include_directories("./includes/")

add_compile_options("$<$<C_COMPILER_ID:MSVC>:/utf-8>")
add_compile_options("$<$<CXX_COMPILER_ID:MSVC>:/utf-8>")

set(MY_EXECUTABLE_NAME "WinCppTemplate")
add_executable(${MY_EXECUTABLE_NAME} "./src/main.cpp")
