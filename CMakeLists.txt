cmake_minimum_required(VERSION 3.24)

project(disable-playerghost
    VERSION 1.0.0
    DESCRIPTION "Mod to prevent playerghost from spawning"
    HOMEPAGE_URL "https://github.com/dextercd/noita-disable-playerghost"
    LANGUAGES CXX
)

install(DIRECTORY disable-playerghost
    DESTINATION .
    COMPONENT disable-playerghost
)

set(CPACK_VERBATIM_VARIABLES TRUE)
set(CPACK_GENERATOR ZIP)
set(CPACK_INCLUDE_TOPLEVEL_DIRECTORY FALSE)
set(CPACK_PACKAGE_FILE_NAME "${PROJECT_NAME}-${PROJECT_VERSION_MAJOR}.${PROJECT_VERSION_MINOR}.${PROJECT_VERSION_PATCH}")
include(CPack)
