include_directories ("${PROJECT_SOURCE_DIR}/lib")
include_directories ("${PROJECT_SOURCE_DIR}/app")

set(demo_SRC demo.c)
add_executable(demo ${demo_SRC})

if(SAPP)
	set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -static")
	set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -static")
	target_link_libraries (demo demolib_s)
else()	
	target_link_libraries (demo demolib)
endif()

# install (TARGETS demo DESTINATION bin)