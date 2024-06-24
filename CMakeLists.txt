cmake_minimum_required(VERSION 3.5)

project(MyProject VERSION 1.0 LANGUAGES CXX)

add_subdirectory(src)

install(TARGETS myproj_bin DESTINATION bin)

set(CPACK_GENERATOR WIX)
set(CPACK_PACKAGE_NAME "MyWixProject")
set(CPACK_PACKAGE_VERSION "1.0.2")
set(CPACK_PACKAGE_INSTALL_DIRECTORY "JMJAtlanta/${CMAKE_PROJECT_NAME}") # where to place the files on disk
set(CPACK_WIX_PROGRAM_MENU_FOLDER "MyWixProject")
# Make the GUID below unique. This helps when upgrading versions of your product
# Make this unique to your version
set(CPACK_WIX_UPGRADE_GUID "1A9911F1-6581-470D-9808-6507B213999B")
# This prevents another installer from installing their product over yours
# Make this unique to your product NOTE: must change each time (or auto-generate by leaving it out)
#set(CPACK_WIX_PRODUCT_GUID "1A9911F1-6581-470D-9808-6507B213999B")
set(CPACK_RESOURCE_FILE_LICENSE "${CMAKE_CURRENT_SOURCE_DIR}/License.txt")
set(CPACK_CREATE_DESKTOP_LINKS myproj_bin) # desktop shortcut
set(CPACK_PACKAGE_EXECUTABLES myproj_bin "MyProject") # name on desktop
include(CPack)

