# TODO: Add project name-getting logic
cmake_minimum_required(VERSION 3.25)

# set(VCPKG_TOOLCHAIN $ENV{VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake CACHE FILEPATH "Path to VCPKG toolchain file")
# set(CMAKE_TOOLCHAIN_FILE ${VCPKG_TOOLCHAIN})
set(CMAKE_TOOLCHAIN_FILE C:/vcpkg/scripts/buildsystems/vcpkg.cmake)
# TODO: Why does it work when explicitly set, but not when queried from (env ->) cache?
set(CMAKE_CXX_STANDARD 17)

project(wxwtest)

find_package(wxWidgets REQUIRED COMPONENTS net core base)

if(wxWidgets_USE_FILE)
  include(${wxWidgets_USE_FILE})
endif()

add_executable(${PROJECT_NAME} ./src/main.cpp)


target_link_libraries(${PROJECT_NAME} ${wxWidgets_LIBRARIES})
set_target_properties(${PROJECT_NAME} PROPERTIES WIN32_EXECUTABLE TRUE)
``
