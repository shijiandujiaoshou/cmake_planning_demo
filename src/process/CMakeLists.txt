project(process)

add_library(
    ${PROJECT_NAME} #把动态库命名为process
    SHARED
    process.cpp
)#将process.cpp变成一个动态库

target_include_directories(
    ${PROJECT_NAME} 
    PUBLIC
    ${PNC_Map_Dir}

)

target_link_libraries(
    ${PROJECT_NAME}
    PUBLIC
    pnc_map

)#将process.cpp这个动态库链接pnc_map这个动态库