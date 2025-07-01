cmake_minimum_required(VERSION 3.10)
project(Space_Invaders)

set(CMAKE_CXX_STANDARD 20)

# Paths to your libraries
set(GLFW_DIR "${CMAKE_SOURCE_DIR}/glfw_3_4_bin_WIN_64")
set(GLEW_DIR "${CMAKE_SOURCE_DIR}/glew_2_1_0")

# Include directories
include_directories(
        ${GLFW_DIR}/include
        ${GLEW_DIR}/include
)

# Link directories - Use the correct MinGW-compatible folder
link_directories(
        ${GLFW_DIR}/lib-mingw-w64
        ${GLEW_DIR}/lib/Release/x64
)

# Add your executable
add_executable(Space_Invaders main.cpp)

# Link required libraries
target_link_libraries(Space_Invaders
        glfw3
        glew32s
        opengl32
)
