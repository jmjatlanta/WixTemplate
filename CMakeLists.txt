cmake_minimum_required(VERSION 3.5)

project(MyProject VERSION 1.0 LANGUAGES CXX)

add_subdirectory(src)

install(TARGETS myproj_bin DESTINATION bin)

set(CPACK_GENERATOR WIX)
set(CPACK_PACKAGE_NAME "MyWixProject")
set(CPACK_PACKAGE_VERSION "1.0.0")
set(CPACK_WIX_PROGRAM_MENU_FOLDER "MyWixProject")
# Make the GUID below unique. This helps when upgrading versions of your product
# Make this unique to your version
set(CPACK_WIX_UPGRADE_GUID "1A9911F1-6581-470D-9808-6507B213999B")
# This prevents another installer from installing their product over yours
# Make this unique to your product
set(CPACK_WIX_PRODUCT_GUID "1A9911F1-6581-470D-9808-6507B213999B")
set(CPACK_WIX_LICENSE_RTF "${CMAKE_CURRENT_SOURCE_DIR}/License.txt")
include(CPack)

