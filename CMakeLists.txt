cmake_minimum_required(VERSION 3.10)

project(TrainingTracker)

set(CMAKE_CXX_STANDARD 17)

include_directories(include)
file(GLOB SOURCES "src/*.cpp")

find_package(OpenCV REQUIRED)

add_executable(TrainingTracker ${SOURCES} )

target_include_directories(TrainingTracker PRIVATE ${OpenCV_INCLUDE_DIRS})
target_link_libraries(TrainingTracker PRIVATE ${OpenCV_LIBS})
