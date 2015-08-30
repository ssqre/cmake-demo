include_directories ("${PROJECT_SOURCE_DIR}/lib")

set(demolib_SRC demolib.c)
add_library(demolib SHARED ${demolib_SRC})
set_target_properties(demolib PROPERTIES VERSION 1.0 SOVERSION 1)

add_library(demolib_s STATIC ${demolib_SRC})
set_target_properties(demolib_s PROPERTIES OUTPUT_NAME "demolib")

# install (TARGETS demolib DESTINATION bin)