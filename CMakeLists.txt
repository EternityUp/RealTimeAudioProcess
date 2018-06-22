cmake_minimum_required(VERSION 2.6)
project(arrayprocesssynthesis)

INCLUDE_DIRECTORIES(/home/xzc/eigen3.3.4/)

add_compile_options(-std=c++11)

LINK_DIRECTORIES(${CMAKE_SOURCE_DIR}/libs/)

add_executable(arrayprocesssynthesis mic_array_processing.cpp main.cpp)

target_link_libraries(arrayprocesssynthesis ArrayShapeAnalysis FourierTransform AudioFileProcess WavFileRW BasicSignalProcess)

install(TARGETS arrayprocesssynthesis RUNTIME DESTINATION bin)
