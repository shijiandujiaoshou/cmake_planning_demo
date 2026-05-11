cmake_minimum_required(VERSION 3.22.1)  
project(planning 
    VERSION 0.0.1
    DESCRIPTION "a demo for cmake planning"
    HOMEPAGE_URL "https://github.com/shijiandujiaoshou/cmake_planning_demo"
    LANGUAGES CXX #指定语言为C++

)  
set(CMAKE_CXX_STANDARD 17) 

#变量设置
set(Process_Dir ${CMAKE_SOURCE_DIR}/src/process)#自定义路径 变量名为自定义的Process_Dir
set(PNC_Map_Dir ${CMAKE_SOURCE_DIR}/src/pnc_map)#自定义路径 变量名为自定义的Process_Dir
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)#指定/创建可执行文件生成目录
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)#把动态库指定到bin目录下
#上面设置的变量也是可以传递到下面的子目录中的，也就是说子目录中的CMakeLists也是可以用到父目录的变量的，简单可以理解为类的继承
#添加子目录
add_subdirectory(src) #即找src目录下的CMakeLists.txt