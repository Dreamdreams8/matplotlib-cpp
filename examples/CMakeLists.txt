cmake_minimum_required(VERSION 3.16)  
project(test)  
 
set(CMAKE_CXX_STANDARD 17) #（选择C++17）
 
find_package(PythonLibs REQUIRED)
#下面两句代码路径要改成你自己的
set(PYTHON_INCLUDE_DIRS /home/***/soft/anaconda3/include/python3.10)
set(PYTHON_LIBRARIES /home/***/soft/anaconda3/lib/libpython3.10.so)
include_directories(${PYTHON_INCLUDE_DIRS})
 
# 添加 Matplotlib 的头文件路径
include_directories(/home/***/demo/matplotlib-cpp/)
 
add_executable(test modern.cpp)
 
# 链接 Python 和 Matplotlib 库
target_link_libraries(test ${PYTHON_LIBRARIES})
