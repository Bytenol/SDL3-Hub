cmake_minimum_required(VERSION 3.10)

project(SDL3-Hub-Small)

add_library(ideps INTERFACE)

target_link_libraries(ideps INTERFACE SDL3::SDL3)

add_executable(SAT SAT.cpp)
target_link_libraries(SAT PRIVATE ideps)

add_executable(raycasting raycasting.cpp)
target_link_libraries(raycasting PRIVATE ideps)

add_executable(pong2d pong2d.cpp)
target_link_libraries(pong2d PRIVATE ideps)

add_executable(tetris tetris.cpp)
target_link_libraries(tetris PRIVATE ideps)

add_executable(archimedes archimedes.cpp)
target_link_libraries(archimedes PRIVATE ideps)

add_executable(sierpienskiTriangle sierpienskiTriangle.cpp)
target_link_libraries(sierpienskiTriangle PRIVATE ideps)


#add_executable(window )
#target_link_libraries(window PRIVATE ideps)