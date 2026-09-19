cmake_minimum_required(VERSION 3.16)
project(samp2_4 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 REQUIRED COMPONENTS Widgets)

qt_standard_project_setup()

qt_add_executable(samp2_4 WIN32
    main.cpp
    qwmainwind.cpp
    qwmainwind.h
    qwmainwind.ui
    res.qrc
)

target_link_libraries(samp2_4 PRIVATE Qt6::Widgets)

set_target_properties(samp2_4 PROPERTIES
    WIN32_EXECUTABLE TRUE
    MACOSX_BUNDLE TRUE
)
