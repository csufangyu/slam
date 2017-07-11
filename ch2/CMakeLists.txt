cmake_minimum_required(VERSION 2.8)
#声明一个cmake工程
project(helloSLAM)
#设置编译模式
set(CMAKE_BUILD_TYPE "Debug")
add_library(hello_shared SHARED libHelloSLAM.cpp)
#add_library( hello libHelloSLAM.cpp )
#添加可执行程序
add_executable(useHello useHello.cpp)
target_link_libraries(useHello hello_shared)

