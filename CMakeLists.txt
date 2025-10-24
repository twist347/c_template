cmake_minimum_required(VERSION 3.20)

set(PROJECT_NAME c_template)

project(${PROJECT_NAME} LANGUAGES C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_executable(${PROJECT_NAME} main.c)
target_link_libraries(${PROJECT_NAME} PRIVATE m)
target_compile_options(${PROJECT_NAME} PRIVATE -Wall -Wextra -Wpedantic)
