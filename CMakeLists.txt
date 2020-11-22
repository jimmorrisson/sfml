cmake_minimum_required(VERSION 3.15)
project(SFML_PROJ)

add_subdirectory(build/SFML/)
set(SFML_DIR build/build/SFML/)
file(GLOB SFML_LIBS  ${SFML_DIR}*)
# set(SFML_STATIC_LIBRARIES TRUE)
# set(SFML_DIR "build/build/SFML/")
# find_package(SFML 2.5 COMPONENTS audio graphics window system REQUIRED)

# add_executable(${PROJECT_NAME} ${SOURCE_FILES})

# target_link_libraries(${PROJECT_NAME} sfml-graphics)
# target_link_libraries(${PROJECT_NAME} sfml-audio)
# include_directories(build/build/SFML/include)

# find_package(SFML 2.5 COMPONENTS graphics audio REQUIRED)

add_executable(${CMAKE_PROJECT_NAME} main.cc)
target_link_libraries(${CMAKE_PROJECT_NAME} sfml-window)