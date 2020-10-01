add_library(cutils-socket SHARED
  sockets.cpp
  sockets_unix.cpp
  socket_network_client_unix.cpp
  socket_inaddr_any_server_unix.cpp
)

target_include_directories(cutils-socket PUBLIC ${PROJECT_SOURCE_DIR}/libcutils/include/
  ${PROJECT_SOURCE_DIR}/libbase/include/
)
