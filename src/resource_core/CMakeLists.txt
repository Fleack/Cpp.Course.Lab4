add_library(resource_core INTERFACE)

target_include_directories(resource_core
        INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_link_libraries(resource_core INTERFACE project_warnings)
if (TARGET project_sanitizers)
        target_link_libraries(resource_core INTERFACE project_sanitizers)
endif ()
