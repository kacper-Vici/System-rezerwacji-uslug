cmake_minimum_required(VERSION 3.16)
project(Uslugi_Fryzjerskie CXX)

set(CMAKE_CXX_STANDARD 17)

# Automatycznie zbiera wszystkie .cpp z src/ oraz podfolderów (np. src/uslugi/)
file(GLOB_RECURSE PATHS src/*.cpp)

# poleca kompilatorowi zbudować jeden główny program wykonywalny o nazwie Uslugi_Fryzjerskie, wykorzystując wszystkie pliki źródłowe zebrane wcześniej w zmiennej ZRODLA
add_executable(Uslugi_Fryzjerskie ${PATHS})

# Pozwala na krótkie #include "Usluga.h" oraz #include "tabulate.hpp" w całym projekcie
target_include_directories(Uslugi_Fryzjerskie PRIVATE src src/uslugi external)

# Obsługa polskich znaków UTF-8 na Windowsie (Visual Studio)
if (MSVC)
    target_compile_options(Uslugi_Fryzjerskie PRIVATE /utf-8)
endif()