cmake_minimum_required(VERSION 3.29.0 FATAL_ERROR)

set(PROJECT_NAME BattleCity)
project(${PROJECT_NAME})

add_executable(${PROJECT_NAME} src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOLL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOLL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOLL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOLL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${PROJECT_NAME} glfw)
