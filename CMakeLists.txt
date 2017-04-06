cmake_minimum_required(VERSION 3.6)
project(Animation)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -framework OPENGL")
set(GLFW3_LIBRARY "/usr/local/lib/libglfw.3.2.dylib")
set(GLEW_LIBRARY "/usr/local/lib/libGLEW.dylib")

set(SOURCE_FILES animation.cpp utils/shader.cpp utils/shader.h)
add_executable(Animation ${SOURCE_FILES})
target_link_libraries(Animation ${GLFW3_LIBRARY} ${GLEW_LIBRARY})