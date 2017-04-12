cmake_minimum_required(VERSION 3.2)
project(sudokuParsedOpenCV)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -lopencv_calib3d -lopencv_core -lopencv_features2d -lopencv_flann -lopencv_highgui -lopencv_imgcodecs -lopencv_imgproc -lopencv_ml -lopencv_objdetect -lopencv_photo -lopencv_shape -lopencv_stitching -lopencv_superres -lopencv_ts -lopencv_video -lopencv_videoio -lopencv_videostab")

set(SOURCE_FILES
    SudokuScanner/main.cpp)


FIND_PACKAGE( OpenCV REQUIRED core highgui imgproc)

add_executable(sudokuParsedOpenCV ${SOURCE_FILES}  SudokuScanner/ImageParserMain/ImageParserMain.cpp SudokuScanner/ImageParserMain/ImageParserMain.h)