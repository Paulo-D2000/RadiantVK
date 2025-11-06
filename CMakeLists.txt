cmake_minimum_required(VERSION 3.10)

project(VulkanExample)

set(CMAKE_CXX_STANDARD 17)

find_package(Vulkan REQUIRED)

add_subdirectory(dependencies/glfw)

add_subdirectory(dependencies/glm)

add_executable(${PROJECT_NAME} 
    src/main.cpp
)

target_include_directories(${PROJECT_NAME} 
    PRIVATE
    dependencies
)

target_link_libraries(${PROJECT_NAME} 
    glm::glm
    glfw
    Vulkan::Vulkan
)
