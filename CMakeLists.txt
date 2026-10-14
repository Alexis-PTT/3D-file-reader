cmake_minimum_required(VERSION 4.2)
project(moteur C)
find_package(SDL3 REQUIRED)

set(CMAKE_C_STANDARD 23)

add_executable(moteur
        3DMotor.c)

add_executable(testWindows
        exGraphic.c
        3DMotor.c
        3DMotor.h
)

target_link_libraries(moteur PRIVATE m)
target_link_libraries(moteur PRIVATE SDL3::SDL3)
target_link_libraries(testWindows PRIVATE m)
target_link_libraries(testWindows PRIVATE SDL3::SDL3)
