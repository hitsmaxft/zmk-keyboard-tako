# Tako Module CMakeLists.txt

# Add the tako_drivers directory to the build
add_subdirectory(tako_drivers)

# Register the boards and dts directories
set(BOARD_ROOT ${CMAKE_CURRENT_LIST_DIR}/boards ${BOARD_ROOT})
set(DTS_ROOT ${CMAKE_CURRENT_LIST_DIR}/dts ${DTS_ROOT})