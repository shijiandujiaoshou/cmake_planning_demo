project(planning_main)
add_subdirectory(pnc_map)
add_subdirectory(process)

#因为main函数在这一层，所以要把main函数添加为可执行文件
add_executable(
    ${PROJECT_NAME}#文件名就用工程名
    planning_main.cpp
)

target_include_directories(
    ${PROJECT_NAME} 
    PUBLIC
    ${Process_Dir}

)

target_link_libraries(
    ${PROJECT_NAME}
    PUBLIC
    process

)