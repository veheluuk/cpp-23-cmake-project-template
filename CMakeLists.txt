cmake_minimum_required(VERSION 3.20)

project(PLACEHOLDER_PROJECT_NAME CXX)

# Output binary executable
add_executable(
  PLACEHOLDER_PROJECT_NAME
  "Main.cpp"
)

set_property(TARGET PLACEHOLDER_PROJECT_NAME PROPERTY CXX_STANDARD 23)							# Compile as C++23 (Visual Studio /std:c++latest)

# Fix C++ version when compiling on Visual Studio (fixes __cplusplus etc.)
if(MSVC)
    target_compile_options(PLACEHOLDER_PROJECT_NAME PUBLIC "/Zc:__cplusplus")
    target_compile_features(PLACEHOLDER_PROJECT_NAME PUBLIC cxx_std_23)								
endif()
