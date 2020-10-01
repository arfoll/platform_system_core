cmake_minimum_required(VERSION 3.18)

project(cmake-fastboot DESCRIPTION "Fastboot built with cmake")

add_subdirectory(libziparchive)
add_subdirectory(diagnose_usb)
add_subdirectory(avb/libavb)
add_subdirectory(liblog)
add_subdirectory(libbase)
add_subdirectory(libcutils)
add_subdirectory(libsparse)
add_subdirectory(fastboot)
