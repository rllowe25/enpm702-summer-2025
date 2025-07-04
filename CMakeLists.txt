cmake_minimum_required(VERSION 3.10.0)
project(enpm702_summer2025 VERSION 0.1.0 LANGUAGES C CXX)

add_compile_options(-Wall)
add_executable(lecture1_cpp lecture1/src/lecture1.cpp)
add_executable(lecture2_cpp lecture2/src/lecture2.cpp)
add_executable(lecture3_cpp lecture3/src/lecture3.cpp)
add_executable(lecture4_cpp lecture4/src/lecture4.cpp)

# Set C++17 standard for the target
set_property(TARGET lecture1_cpp PROPERTY CXX_STANDARD 17)
set_property(TARGET lecture1_cpp PROPERTY CXX_STANDARD_REQUIRED ON)
set_property(TARGET lecture2_cpp PROPERTY CXX_STANDARD 17)
set_property(TARGET lecture2_cpp PROPERTY CXX_STANDARD_REQUIRED ON)
set_property(TARGET lecture3_cpp PROPERTY CXX_STANDARD 17)
set_property(TARGET lecture3_cpp PROPERTY CXX_STANDARD_REQUIRED ON)
set_property(TARGET lecture4_cpp PROPERTY CXX_STANDARD 17)
set_property(TARGET lecture4_cpp PROPERTY CXX_STANDARD_REQUIRED ON)


# Add Valgrind target for lecture3_cpp
# find_program(VALGRIND_EXECUTABLE valgrind)
# if(VALGRIND_EXECUTABLE)
#     add_custom_target(valgrind_lecture3
#         COMMAND ${VALGRIND_EXECUTABLE} --tool=memcheck --leak-check=full --show-leak-kinds=all --track-origins=yes $<TARGET_FILE:lecture3_cpp>
#         DEPENDS lecture3_cpp
#         COMMENT "Running Valgrind on lecture3_cpp"
#     )
# endif()