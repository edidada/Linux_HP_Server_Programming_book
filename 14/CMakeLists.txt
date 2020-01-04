add_executable(14-1mutual_lock 14-1mutual_lock.c)

find_package(Threads REQUIRED)
target_link_libraries(14-1mutual_lock Threads::Threads)