cmake_minimum_required(VERSION 3.10)
project(YourProjectName)

# 设置C++14标准
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# 查找Eigen3库
find_package(Eigen3 REQUIRED)

include_directories(/usr/local/include /opt/homebrew/include/)

# 添加可执行文件
add_executable(Transformation main.cpp)

# 链接Eigen库
target_link_libraries(Transformation Eigen3::Eigen)