cmake_minimum_required(VERSION 3.28)

project(Hello_WxWidgets)

set (wxWidgets_ROOT_DIR  "C:/Program Files (x86)/wxWidgets")
set (wxWidgets_LIB_DIR  "C:/Program Files (x86)/wxWidgets/lib/gcc_dll")
find_package(wxWidgets REQUIRED COMPONENTS net core base)
include(${wxWidgets_USE_FILE})



file(GLOB project_GLOB
src/*)

add_executable(Hello ${project_GLOB})


target_link_libraries(Hello ${wxWidgets_LIBRARIES})
target_include_directories(Hello PRIVATE ${wxWidgets_INCLUDE_DIRECTORIES})