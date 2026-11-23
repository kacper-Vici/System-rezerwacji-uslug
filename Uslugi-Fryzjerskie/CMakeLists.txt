cmake_minimum_required(VERSION 4.3)
project(Uslugi_Fryzjerskie)

set(CMAKE_CXX_STANDARD 20)

add_executable(Uslugi_Fryzjerskie src/main.cpp
        src/uslugi/usluga.cpp
        src/uslugi/usluga.h
        src/uslugi/Strzyzenie.cpp
        src/uslugi/Strzyzenie.h
        src/uslugi/Koloryzacja.cpp
        src/uslugi/Koloryzacja.h
        src/uslugi/Stylizacja.cpp
        src/uslugi/Stylizacja.h)
