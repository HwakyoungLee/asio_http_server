cmake_minimum_required(VERSION 2.8)
project(suibian)

aux_source_directory(. allsrc)
include_directories(/opt/boost/include)

link_directories(/opt/boost/lib)
link_directories(/usr/lib/x86_64-linux-gnu)
link_libraries(boost_thread)
link_libraries(boost_date_time)
link_libraries(boost_system)
link_libraries(boost_program_options)
link_libraries(boost_filesystem)
link_libraries(pthread)

add_executable(server ${allsrc})
#target_link_libraries(boost_thread boost_date_time boost_system boost_program_options boost_filesystem)
