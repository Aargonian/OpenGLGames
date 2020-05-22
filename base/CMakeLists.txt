cmake_minimum_required(VERSION 3.00)

set(BASE_SOURCE src/main.c)

add_executable(base ${BASE_SOURCE})

target_link_libraries(base PRIVATE EmberLib)
target_link_libraries(base PRIVATE glad)
target_link_libraries(base PRIVATE glfw)
