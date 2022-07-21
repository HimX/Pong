cmake_minimum_required(VERSION 3.22)
project(Pong)

set(SFML_STATIC_LIBRARIES TRUE)
set(CMAKE_CXX_STANDARD 14)
find_package(SFML 2.5 COMPONENTS system window graphics audio network REQUIRED)

add_executable(Pong main.cpp Bat.cpp Bat.h Ball.cpp Ball.h)
target_link_libraries(Pong sfml-system sfml-window sfml-graphics sfml-audio sfml-network -static)
