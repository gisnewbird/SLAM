#声明要求的cmake最低版本
cmake_minimum_required( VERSION 2.8 )

#声明一个cmake工程
project( helloslam )

#添加一个可执行程序
#add_executable(hello hello.cpp)

#添加cpp文件成一个共享库
add_library(hello_shared SHARED libHello.cpp)

#使用共享库文件测试
add_executable(helloTest useHello.cpp)
target_link_libraries(helloTest /home/duke/文档/slam/libhello_shared.so)
