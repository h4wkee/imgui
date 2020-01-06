cmake_minimum_required(VERSION 3.15)
project(imgui)

set(CMAKE_CXX_STANDARD 17)

file(GLOB SRC_FILES *.cpp)

add_library(imgui STATIC ${SRC_FILES} examples/imgui_impl_glfw.cpp examples/imgui_impl_opengl3.cpp)

target_compile_definitions(imgui PUBLIC IMGUI_IMPL_OPENGL_LOADER_GLAD)