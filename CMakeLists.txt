cmake_minimum_required(VERSION 3.9)
PROJECT (opencv_contrib)
find_package(OpenCV REQUIRED)
set( NAME_SRC
        modules/aruco/samples/detect_board.cpp)

set( NAME_HEADERS
        include/header.h
        )

INCLUDE_DIRECTORIES( ${CMAKCMAKE_BINARY_DIRE_CURRENT_SOURCE_DIR}/include )
link_directories( ${CMAKE_BINARY_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)
add_executable( opencv_contrib ${NAME_SRC})
target_link_libraries( opencv_contrib ${OpenCV_LIBS})