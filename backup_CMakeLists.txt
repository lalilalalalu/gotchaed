cmake_minimum_required(VERSION 3.25)
project(gotchaED C)

set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake;${CMAKE_MODULE_PATH}")

find_package(GOTCHA REQUIRED)


add_executable(gotchaED main.c)

target_link_libraries(gotchaED PRIVATE ${GOTCHA_LIBRARIES})
target_compile_features(gotchaED PRIVATE c_std_11)
message(STATUS ${GOTCHA_LIBRARIES})
message(STATUS ${GOTCHA_INCLUDE_DIRS})
target_include_directories(gotchaED PRIVATE ${GOTCHA_INCLUDE_DIRS})
