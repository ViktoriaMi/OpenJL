cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

set(PROJECT_NAME "My_trial_project")
set(EXECUTABLE_NAME "My_trial_project")

project(${PROJECT_NAME})

add_executable(${EXECUTABLE_NAME} src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${PROJECT_NAME} glfw)