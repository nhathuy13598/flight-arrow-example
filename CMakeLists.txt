cmake_minimum_required(VERSION 3.16)

project(flight-arrow-example)

find_package(Arrow REQUIRED)

add_executable(arrow_example arrow_example.cpp)
target_link_libraries(arrow_example PRIVATE Arrow::arrow_shared)

add_executable(flight_server flight_server.cpp)
target_link_libraries(flight_server PRIVATE Arrow::arrow_shared)

add_executable(flight_client flight_client.cpp)
target_link_libraries(flight_client PRIVATE Arrow::arrow_shared)