cmake_minimum_required(VERSION 3.22)
project(ACMSIM C)

set(CMAKE_C_STANDARD 99)

add_executable(ACMSIM main.c ACMSim.h observer.c observer.h controller.c controller.h ACMPlot.py)


#include_directories(../venv/Include)
#link_libraries(../python39.lib)
# 如果使用的是非系统目录下的 Python 可以通过指定 Python3_ROOT_DIR 改变查找路径
set(Python3_ROOT_DIR "${CMAKE_SOURCE_DIR}/venv")
find_package(Python3 COMPONENTS Interpreter Development REQUIRED)
target_include_directories(${PROJECT_NAME} PRIVATE ${Python3_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} ${Python3_LIBRARIES})
