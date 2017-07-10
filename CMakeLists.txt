cmake_minimum_required(VERSION 3.7)
project(wm_ArduinoLibrary)

set(CMAKE_CXX_STANDARD 11)

set(ArCom_SOURCE_FILES
		ArCom/src/main.cpp
		ArCom/src/library/ArCom_Main.cpp)

add_executable(ArComTest ${ArCom_SOURCE_FILES})