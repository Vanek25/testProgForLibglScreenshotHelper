cmake_minimum_required(VERSION 3.18)

project(test) 

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(test main.cpp)

find_package(glfw3 3.3 REQUIRED)
find_package(OpenGL REQUIRED)

find_library(LIB_glScreenshotHelper glScreenshotHelper)
find_library(LIB_freeimage freeimage)
find_library(LIB_cppunit cppunit)

target_link_libraries(${PROJECT_NAME} glScreenshotHelper freeimage cppunit ${OPENGL_LIBRARIES} glfw)

