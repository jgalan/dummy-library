set( LibraryVersion "1.0" )
add_definitions(-DLIBRARY_VERSION="${LibraryVersion}")

## This CMakeLists file integrates the compilation of this library inside the main REST-for-Physics framework compilation system.
## It defines the installation of macros, examples and data directories into the main REST_PATH.

## Have a look at other REST libraries for hints on how to integrate new dependencies, or compilation options.

COMPILELIB("")

file(GLOB_RECURSE MAC "${CMAKE_CURRENT_SOURCE_DIR}/macros/*")
INSTALL(FILES ${MAC} DESTINATION ./macros/dummy)

file(GLOB_RECURSE EXPL "${CMAKE_CURRENT_SOURCE_DIR}/examples/*")
INSTALL(FILES ${MAC} DESTINATION ./examples/dummy)

file(GLOB_RECURSE DATA "${CMAKE_CURRENT_SOURCE_DIR}/data/*")
INSTALL(FILES ${MAC} DESTINATION ./data/dummy)
