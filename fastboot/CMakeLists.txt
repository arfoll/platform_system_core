add_library(fastboot SHARED
  bootimg_utils.cpp
  fs.cpp
  socket.cpp
  tcp.cpp
  udp.cpp
  util.cpp
  fastboot_driver.cpp
  usb_linux.cpp
  fastboot.cpp
)

target_compile_features(fastboot PRIVATE cxx_std_17)

target_include_directories(fastboot PUBLIC
  ${PROJECT_SOURCE_DIR}/libsparse/include/
  ${PROJECT_SOURCE_DIR}/libbase/include/
  ${PROJECT_SOURCE_DIR}/avb/
  ${PROJECT_SOURCE_DIR}/mkbootimg/include/bootimg/
  ${PROJECT_SOURCE_DIR}/include
  ${PROJECT_SOURCE_DIR}/diagnose_usb/include
  ${PROJECT_SOURCE_DIR}/libziparchive/include
)

set_target_properties(fastboot PROPERTIES PUBLIC_HEADER include/sparse/sparse.h)

target_link_libraries(fastboot cutils-socket sparse base log avb ziparchive diagnose_usb)

add_executable(fastbootcli
  main.cpp
)

target_link_libraries(fastbootcli fastboot)
