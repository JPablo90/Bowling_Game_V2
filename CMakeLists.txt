cmake_minimum_required(VERSION 3.20)

project(Bowling_Game)

# 1. Configurar GoogleTest
include(FetchContent)
FetchContent_Declare(
  googletest
  URL https://github.com/google/googletest/archive/refs/tags/v1.14.0.zip
)
# Para forzar el uso de la misma runtime library (MSVC)
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
FetchContent_MakeAvailable(googletest)

# 2. Habilitar pruebas
enable_testing()

set(TESTBOL tests/main_test.cpp tests/Quadrant_test.cpp tests/Bowling_Game_test.cpp)

# 3. Añadir tu ejecutable de pruebas
add_executable(runTests ${TESTBOL})

# 4. Enlazar GoogleTest
target_link_libraries(runTests GTest::gtest_main)

# 5. Descubrir pruebas (para CTest)
include(GoogleTest)
gtest_discover_tests(runTests)

add_definitions(-std=c++11)

add_definitions(-Wall)

include_directories(include)

set(SRCBOL src/main.cpp src/Quadrant.cpp src/Bowling_Game.cpp)

# 1. Create the executable with a valid name
add_executable(Bowling ${SRCBOL})

# 2. Tell CMake to put the resulting binary in your specific folder
set_target_properties(Bowling PROPERTIES 
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/bin"
)
