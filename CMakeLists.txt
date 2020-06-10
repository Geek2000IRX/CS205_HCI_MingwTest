cmake_minimum_required(VERSION 3.16)
project(CS205_HCI_MingwTest)
set(CMAKE_CXX_STANDARD 14)
set(OpenCV_INCLUDE_DIRS
        D:/C-Projects/opencv-4.2.0/include/opencv2)
set(HighGUI_INCLUDE_DIRS
        D:/C-Projects/opencv-4.2.0/modules/highgui/include/opencv2)
set(ImgProc_INCLUDE_DIRS
        D:/C-Projects/opencv-4.2.0/modules/imgproc/include/opencv2)
set(Core_INCLUDE_DIRS
        D:/C-Projects/opencv-4.2.0/modules/core/include/opencv2/core)
FIND_PACKAGE(OpenCV REQUIRED)
message(STATUS "OpenCV library status:")
message(STATUS " version: ${OpenCV_VERSION}")
message(STATUS " libraries: ${OpenCV_LIBS}")
message(STATUS " include path: ${OpenCV_INCLUDE_DIRS} ${HighGUI_INCLUDE_DIRS} ${ImgProc_INCLUDE_DIRS} ${Core_INCLUDE_DIRS}")
include_directories(
        ${PROJECT_SOURCE_DIR}
        ${OpenCV_INCLUDE_DIRS}
        ${HighGUI_INCLUDE_DIRS}
        ${ImgProc_INCLUDE_DIRS}
        ${Core_INCLUDE_DIRS}
        "D:/C-Projects/opencv-4.2.0/include/opencv2"
)
#include_directories(${OpenCV_INCLUDE_DIRS})
add_executable(CS205_HCI_MingwTest main.cpp)
target_link_libraries(CS205_HCI_MingwTest ${OpenCV_LIBS})

