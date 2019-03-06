cmake_minimum_required (VERSION 2.8.11)
project (coolprop_fortran)
enable_language(Fortran)

# Add CoolProp dependency
set(COOLPROP_SHARED_LIBRARY true CACHE INTERNAL "Build CoolProp shared library (a DLL)")
add_subdirectory ("${CMAKE_CURRENT_SOURCE_DIR}/externals/coolprop" "coolprop")

# Add code for fortran 
add_executable(main "${CMAKE_CURRENT_SOURCE_DIR}/example.for")
target_link_libraries(main CoolProp)