# Tako Module CMakeLists.txt

# Add the tako_drivers directory to the build only if TAKO_KSCAN_DRIVER is enabled
if(CONFIG_TAKO_KSCAN_DRIVER)
    add_subdirectory(tako_drivers)
endif()

# Register the boards and dts directories
set(BOARD_ROOT ${CMAKE_CURRENT_LIST_DIR}/boards ${BOARD_ROOT})
set(DTS_ROOT ${CMAKE_CURRENT_LIST_DIR}/dts ${DTS_ROOT})