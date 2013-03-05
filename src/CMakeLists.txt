#
#Link
#
if (MSVC10)
	add_definitions(-D_LIB;-DUNICODE;-D_UNICODE)
endif()

#
# Include dependencies
#
if (MSVC10)
	include_directories(../sqlite3)
endif()

#
# Source files
#
file(GLOB sources_hpp *.hpp *.h)
file(GLOB sources_cpp *.cpp)
set(sources ${sources_cpp} ${sources_hpp})

#
# Target
#
set(TARGET_NAME hiberlite)
add_library(${TARGET_NAME} ${sources})
