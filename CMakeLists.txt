cmake_minimum_required(VERSION 3.28)

set(CMAKE_DISABLE_IN_SOURCE_BUILD ON)
set(EXPORT_COMPILE_COMMANDS ON)

project(csv CXX)

add_library(csv_parser STATIC)
target_compile_features(csv_parser PUBLIC cxx_std_20)
target_sources(
    csv_parser
    PUBLIC FILE_SET
           module_csv_parser
           TYPE
           CXX_MODULES
           FILES
           mod.cppm)
