cmake_minimum_required(VERSION 3.20)

project(caisse
    VERSION 0.1.0
    DESCRIPTION "Application de caisse (C++ / Qt / SQLite)"
    LANGUAGES CXX
)

# Standard C++ : C++23
# std::format, std::expected, concepts, ranges).
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(caisse app/main.cpp)
target_include_directories(caisse PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)