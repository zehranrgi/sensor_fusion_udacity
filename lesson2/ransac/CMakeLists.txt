cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

add_definitions(-std=c++11)

set(CXX_FLAGS "-Wall")
set(CMAKE_CXX_FLAGS, "${CXX_FLAGS}")
set(Qt5_DIR /opt/homebrew/Cellar/qt@5/5.15.10/lib/cmake/Qt5)

project(playback)

find_package(PCL 1.13 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})
list(REMOVE_ITEM PCL_LIBRARIES "vtkproj4")


add_executable (quizRansac ransac3d_edit.cpp ../../render/render.cpp)
target_link_libraries (quizRansac ${PCL_LIBRARIES})




