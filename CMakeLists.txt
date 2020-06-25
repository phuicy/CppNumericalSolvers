cmake_minimum_required(VERSION 2.8)
project(CppNumericalSolvers)


# Eigen3 Headerfiles
find_package(Eigen3 REQUIRED)
include_directories(SYSTEM ${EIGEN3_INCLUDE_DIR})



add_library(CppNumericalSolvers INTERFACE)
target_include_directories(CppNumericalSolvers INTERFACE
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
)

target_link_libraries(CppNumericalSolvers INTERFACE Eigen3:Eigen)