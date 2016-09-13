cmake_minimum_required(VERSION 2.8)
project(ProgressBar)

include_directories(include)

add_library(progressbar lib/progressbar.c)
add_library(statusbar lib/statusbar.c)

add_executable(demo test/demo.c)
target_link_libraries(demo progressbar statusbar ncurses)
