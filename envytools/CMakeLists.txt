project(ENVYTOOLS C)
cmake_minimum_required(VERSION 2.6)
enable_testing()

SET(CMAKE_C_FLAGS "-g -O2 -Wall")

include_directories(include)

add_subdirectory(util)
add_subdirectory(rnn)

install(DIRECTORY include/ DESTINATION include/envytools)
install(DIRECTORY rnndb DESTINATION share)
install(DIRECTORY hwdocs DESTINATION share/doc/envytools)
install(FILES README DESTINATION share/doc/envytools)
