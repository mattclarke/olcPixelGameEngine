cmake_minimum_required(VERSION 3.19)
project(olcPixelGameEngine)

set(CMAKE_CXX_STANDARD 17)

find_package(PNG REQUIRED)
include_directories(${PNG_INCLUDE_DIR})

add_executable(olcPixelGameEngineExample olcExampleProgram.cpp olcPixelGameEngine.h)
target_link_libraries(olcPixelGameEngineExample
        PNG::PNG
        "-framework Carbon"
        "-framework GLUT"
        "-framework OpenGL"
        )
