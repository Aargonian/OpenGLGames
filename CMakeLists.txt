cmake_minimum_required(VERSION 3.0)
project(OpenGLGames C)

set(CMAKE_C_STANDARD 99)

# External Dependencies

execute_process(COMMAND git submodule update --init --recursive WORKING_DIRECTORY ${CMAKE_SOURCE_DIR})
add_subdirectory(lib/EmberLib)
add_subdirectory(lib/glad)

# We want GLFW but not its docs/tests/examples/etc
set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
add_subdirectory(lib/glfw)

# The Games
add_subdirectory(pong)
