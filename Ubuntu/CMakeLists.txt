cmake_minimum_required(VERSION 3.10)
project(DLtrain)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Specify the compiler explicitly for Linux (if needed)
set(CMAKE_C_COMPILER "/usr/bin/gcc-13")
set(CMAKE_CXX_COMPILER "/usr/bin/g++-13")

# Add source files
set(SOURCES
    main.cpp
    matrix.cpp
    MNISTRead.cpp
    CNN.cpp
)

# Add the executable
add_executable(${PROJECT_NAME} ${SOURCES})

# Include additional compiler flags
target_compile_options(${PROJECT_NAME} PRIVATE
    -fdiagnostics-color=always
    -g # Debugging information
)

# Link the standard C++ library (if required)
target_link_libraries(${PROJECT_NAME} PRIVATE stdc++)

# Add additional arguments (for example to run with arguments)
set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -rdynamic")

# Optionally, set the arguments that you would run your executable with
# You can set the arguments when running the binary through gdb or directly in terminal
# Example for CMake (though typically you'd pass arguments when running the binary)
add_custom_target(run ALL
    COMMAND ${PROJECT_NAME} -m train -s Network1.dat -c config.txt -n 2000 -e 30 -d Images/
    DEPENDS ${PROJECT_NAME}
)
