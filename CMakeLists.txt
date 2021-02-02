cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)
project(hello_webusb)
pico_sdk_init()


add_executable(hello_webusb
    src/main.c
    src/usb_descriptors.c
)

target_include_directories(hello_webusb PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)

# Pull in our pico_stdlib which aggregates commonly used features
target_link_libraries(hello_webusb
    pico_stdlib
    tinyusb_device
)

# create map/bin/hex/uf2 file etc.
pico_add_extra_outputs(hello_webusb)
