cmake_minimum_required(VERSION 3.24)
project(test1)

set(CMAKE_CXX_STANDARD 17)
find_package(Vulkan REQUIRED)

add_executable(test1 main.cpp)

target_link_libraries(test1 PUBLIC Vulkan::Vulkan)
target_link_libraries(test1 PUBLIC "C:/Program Files/bin/glfw-3.3.8.bin.WIN64/lib-mingw-w64/libglfw3.a")

target_include_directories(test1 PUBLIC ${Vulkan_INCLUDE_DIRS})
target_include_directories(test1 PUBLIC "C:/Program Files/bin/glfw-3.3.8.bin.WIN64/include")
target_include_directories(test1 PUBLIC "C:/Program Files/bin/glm")
