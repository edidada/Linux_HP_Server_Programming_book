cmake_minimum_required(VERSION 3.13)
project(linux_hp_book)

set(CMAKE_CXX_STANDARD 11)

#SET(CMAKE_CXX_FLAGS -pthread)

add_subdirectory(5)
add_subdirectory(6)
add_subdirectory(7)
add_subdirectory(8)
add_subdirectory(9)
add_subdirectory(10)
add_subdirectory(11)
add_subdirectory(12)
add_subdirectory(13)
add_subdirectory(14)
add_subdirectory(springsnail)

add_executable(book main.cpp)
add_executable(mutual_lock mutual_lock.c)
add_executable(sigmask sigmask.c)
add_executable(thread_atfork thread_atfork.c)
add_executable(14-3thread_atfork 14/14-3thread_atfork.c)
add_executable(14-5sigmask 14/14-5sigmask.c)
add_executable(15-2pool_cgi 15/15-2pool_cgi.cpp)
add_executable(15-6main 15/15-5http_conn.cpp 15/15-6main.cpp)
add_executable(16-4stress_client 16/16-4stress_client.cpp)

find_package(Threads REQUIRED)

target_link_libraries(sigmask Threads::Threads)
target_link_libraries(thread_atfork Threads::Threads)

target_link_libraries(14-3thread_atfork Threads::Threads)

target_link_libraries(14-5sigmask Threads::Threads)
target_link_libraries(15-6main Threads::Threads)
target_link_libraries(16-4stress_client Threads::Threads)