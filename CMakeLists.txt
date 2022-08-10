

cmake_minimum_required(VERSION 3.1)
project(opencv_example_project)

find_package(OpenCV REQUIRED)

message(STATUS "OpenCV library status:")
message(STATUS "    config: ${OpenCV_DIR}")
message(STATUS "    version: ${OpenCV_VERSION}")
message(STATUS "    libraries: ${OpenCV_LIBS}")
message(STATUS "    include path: ${OpenCV_INCLUDE_DIRS}")

add_executable(${PROJECT_NAME}.exe main.cxx)
target_link_libraries(${PROJECT_NAME}.exe PRIVATE ${OpenCV_LIBS})
