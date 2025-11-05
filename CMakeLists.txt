cmake_minimum_required(VERSION 3.10)

project(VulkanExample)

set(CMAKE_CXX_STANDARD 17)

find_package(Vulkan REQUIRED)

add_executable(${PROJECT_NAME} src/main.cpp)

target_link_libraries(${PROJECT_NAME} Vulkan::Vulkan)
