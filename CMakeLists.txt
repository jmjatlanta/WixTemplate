cmake_minimum_required(VERSION 3.5)

project(MyProject VERSION 1.0 LANGUAGES CXX)

add_subdirectory(src)

install(TARGETS myproj_bin DESTINATION bin)

set(CPACK_GENERATOR WIX)
include(CPack)
set(CPACK_PACKAGE_NAME "MyWixProject")
set(CPACK_PACKAGE_VERSION "1.0.0")
set(CPACK_WIX_PROGRAM_MENU_FOLDER "My Wix Project")

