project(villa-connector)
cmake_minimum_required(VERSION 3.1)


find_library(SYSTEMD_LIBRARIES NAMES systemd)
message("systemd libraries: ${SYSTEMD_LIBRARIES}")

set(LIBVILLACONNECTOR_VERSION_MAJOR 0)
set(LIBVILLACONNECTOR_VERSION_MINOR 1)
set(LIBVILLACONNECTOR_VERSION_PATCH 0)
set(LIBVILLACONNECTOR_VERSION_STRING ${LIBVILLACONNECTOR_VERSION_MAJOR}.${LIBVILLACONNECTOR_VERSION_MINOR}.${LIBVILLACONNECTOR_VERSION_PATCH})

include_directories(
    ${PROJECT_SOURCE_DIR}/include
)

add_subdirectory(src)

install(DIRECTORY include/villa-connector DESTINATION include)
