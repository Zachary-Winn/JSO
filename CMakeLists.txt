cmake_minimum_required (VERSION 3.2)
project (jSO)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Set C++11 as the required standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Set compiler specific options
if (MSVC)
  add_compile_options(/MP /Gm- /W4)
else()
  add_compile_options(-Wall -Wextra -Wpedantic -g)
endif(MSVC)

add_executable(run_tests tests/run_tests.cpp tests/integration_tests.cpp)
