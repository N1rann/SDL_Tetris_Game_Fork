cmake_minimum_required(VERSION 3.16)
project(DeepDiver CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(SDL3 REQUIRED CONFIG)
find_package(SDL3_image REQUIRED CONFIG)

add_executable(MySdlGame src/main_tetris.cpp)

target_link_libraries(MySdlGame PRIVATE
    SDL3::SDL3
    SDL3_image::SDL3_image
)