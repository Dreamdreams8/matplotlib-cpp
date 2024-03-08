# matplotlib-cpp
修改CMakeLists.txt
#下面两句代码路径要改成你自己的
set(PYTHON_INCLUDE_DIRS /home/***/soft/anaconda3/include/python3.10)
set(PYTHON_LIBRARIES /home/***/soft/anaconda3/lib/libpython3.10.so)
 
# 添加 Matplotlib 的头文件路径
include_directories(/home/***/demo/matplotlib-cpp/)

# 直接执行如下命令：
cd example
mkdir build && cd build
cmake ..
make
./test

# 具体流程可参考：

