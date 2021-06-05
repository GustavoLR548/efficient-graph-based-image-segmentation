cmake_minimum_required(VERSION 3.0)
project(ImageSegmentation)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
find_package(OpenCV REQUIRED)
find_package(VTK REQUIRED)
add_executable(ImageSegmentation main.cpp EGBS.cpp EGBS.h graph.cpp graph.h DisjointSet.cpp DisjointSet.h)


message(STATUS " include_path: ${OpenCV_INCLUDE_DIRS}")
include_directories(${OpenCV_INCLUDE_DIRS})
target_link_libraries(ImageSegmentation PUBLIC ${OpenCV_LIBS})
message(STATUS " Libraries: ${OpenCV_LIBS}")
