cmake_minimum_required(VERSION 3.16)
set(CMAKE_C_STANDART 11)
set(CMAKE_CXX_STANDARD 17)
project (test C CXX ASM)
add_executable( test 
                test.c
                aes.c)

target_link_libraries(  test
                        )

target_sources(${PROJECT_NAME}
    PRIVATE
        ${CMAKE_CURRENT_LIST_DIR}/aes.c
    INTERFACE
        ${CMAKE_CURRENT_LIST_DIR}/aes.h
         ${CMAKE_CURRENT_LIST_DIR}/aes.hpp)