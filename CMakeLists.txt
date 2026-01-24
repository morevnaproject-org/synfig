cmake_minimum_required(VERSION 2.8)

project(synfig-studio)

option(ENABLE_UPDATE_CHECKER "Enable online update checker functionality" OFF)
add_subdirectory(ETL)
include_directories(ETL)
include_directories(${PROJECT_BINARY_DIR}/ETL) # to find the generated etl_profile.h
add_subdirectory(synfig-core)

include_directories(synfig-core/src)
add_subdirectory(synfig-studio)