cmake_minimum_required(VERSION 3.00)

set(PONG_SOURCE src/main.c)

add_executable(pong ${PONG_SOURCE})

target_link_libraries(pong PRIVATE EmberLib)
target_link_libraries(pong PRIVATE glad)
target_link_libraries(pong PRIVATE glfw)
