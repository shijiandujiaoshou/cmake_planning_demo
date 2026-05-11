project(pnc_map)

add_library(
    ${PROJECT_NAME} #把动态库命名为pnc_map
    SHARED
    pnc_map.cpp
)#pnc_map.cpp变成一个动态库

#这里就不用在去包含头文件和链接动态库了