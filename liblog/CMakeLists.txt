add_library(log SHARED
  log_event_list.cpp
  log_event_write.cpp
  logger_name.cpp
  logger_read.cpp
  logger_write.cpp
  logprint.cpp
  properties.cpp
)

target_include_directories(log PUBLIC
  ${PROJECT_SOURCE_DIR}/liblog/include/
  ${PROJECT_SOURCE_DIR}/libbase/include/
  ${PROJECT_SOURCE_DIR}/include/
)

target_compile_features(log PRIVATE cxx_std_17)

target_link_libraries(log PRIVATE atomic)
