cmake_minimum_required(VERSION 3.10)

project(openGL VERSION 0.1 LANGUAGES C)

add_executable(openGL
	src/main.c
	src/gl.c
	)

find_library(glfw glfw)
target_link_libraries(openGL PUBLIC ${glfw} m)

target_include_directories(openGL PUBLIC
	"${PROJECT_SOURCE_DIR}/include"
	)
