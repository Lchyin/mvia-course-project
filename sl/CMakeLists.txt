

# cmake所需的最低版本
cmake_minimum_required(VERSION 2.8)

# 设置项目名称
project(mysl)
# 设置C++11文件
set(CMAKE_CXX_SEANDARD 11)
# 寻找opencv库
find_package(Curses REQUIRED)

# 加入opencv头文件
include_directories(${CURSES_INCLUDE_DIRS})

# 添加所需要的输出程序和所需的源文件
add_executable(sl sl.c)
# 将opencv的库链接到程序中
target_link_libraries(sl   ${CURSES_LIBRARIES})

