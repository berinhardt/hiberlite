#
#Link
#
if (MSVC10)
	add_definitions(-D_LIB;-DUNICODE;-D_UNICODE)
endif()

#
# Source files
#
file(GLOB sources_hpp gen-cpp/*.h *.h)
file(GLOB sources_cpp gen-cpp/*.cpp *.cpp)
set(sources ${sources_cpp} ${sources_hpp})

#
# Target
#
set(TARGET_NAME common)
add_library(${TARGET_NAME} ${sources})
