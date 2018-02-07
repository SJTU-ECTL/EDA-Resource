cmake_minimum_required(VERSION 3.8)
project(ectl_research_resource VERSION 0.1.0)
set(CMAKE_CXX_STANDARD 17)

add_library(resource dummy.cpp)

target_compile_definitions(resource
        PUBLIC RESOURCE_BASE_DIR="resource"
        PUBLIC CIRCUIT_BASE_DIR="circuit"
        PUBLIC TECHMAP_BASE_DIR="techmap"
)