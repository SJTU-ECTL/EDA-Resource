cmake_minimum_required(VERSION 3.8)
project(ectl_research_resource VERSION 0.1.0)
set(CMAKE_CXX_STANDARD 17)

set(PROJECT_NAME "resource")

message(STATUS "Loading resources library: '${PROJECT_NAME}'")

add_library(${PROJECT_NAME} dummy.cpp)

target_compile_definitions(${PROJECT_NAME}
        PUBLIC RESOURCE_BASE_DIR="${PROJECT_SOURCE_DIR}"
        PUBLIC CIRCUIT_BASE_DIR="circuit"
        PUBLIC TECHMAP_BASE_DIR="techmap"
)
get_target_property(definitions
        ${PROJECT_NAME} COMPILE_DEFINITIONS )

foreach(def ${definitions})
    message(STATUS "\t[Build Definition ] '${def}'")
endforeach()