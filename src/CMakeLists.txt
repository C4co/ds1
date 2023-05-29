# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(ds1_library VERSION 0.0.1 LANGUAGES C)

add_library(ds1 SHARED
  "ds1.c"
)

set_target_properties(ds1 PROPERTIES
  PUBLIC_HEADER ds1.h
  OUTPUT_NAME "ds1"
)

target_compile_definitions(ds1 PUBLIC DART_SHARED_LIB)
