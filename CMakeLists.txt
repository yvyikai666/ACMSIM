cmake_minimum_required(VERSION 3.22)
project(ACMSIM C)

set(CMAKE_C_STANDARD 99)

add_executable(ACMSIM main.c ACMSim.h observer.c observer.h controller.c controller.h)


#include_directories(../venv/Include)
#link_libraries(C:/Users/YVYIKAI/anaconda3/libs/python39.lib)