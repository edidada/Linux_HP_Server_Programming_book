cmake_minimum_required(VERSION 3.13)
project(book)

set(CMAKE_CXX_STANDARD 11)

add_executable(book main.cpp)
add_executable(mutual_lock mutual_lock.c)
add_executable(sigmask sigmask.c)
add_executable(thread_atfork thread_atfork.c)