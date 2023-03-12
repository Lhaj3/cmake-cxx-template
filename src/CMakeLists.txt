cmake_minimum_required (VERSION 3.8)

file(GLOB_RECURSE PROJECT_CPP_FILES ${PROJECT_SOURCE_DIR}/src *.cpp)
file(GLOB_RECURSE PROJECT_H_FILES ${PROJECT_SOURCE_DIR}/src *.h)

add_executable (main ${PROJECT_CPP_FILES} ${PROJECT_H_FILES} )

target_compile_definitions(main PUBLIC ASSETS_PATH="${PROJECT_SOURCE_DIR}/resources/")
target_include_directories(main PRIVATE ${PROJECT_SOURCE_DIR}/src)
target_include_directories(main PRIVATE ${PROJECT_SOURCE_DIR}/dependencies/include)
# target_link_libraries(main PRIVATE ${PROJECT_SOURCE_DIR}/dependencies/lib/example/example.lib)