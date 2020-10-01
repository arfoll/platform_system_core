add_library(base SHARED
  strings.cpp
  stringprintf.cpp
  logging.cpp
  errors_unix.cpp
  mapped_file.cpp
  file.cpp
  threads.cpp
  liblog_symbols.cpp
  parsenetaddress.cpp
)

target_compile_features(base PRIVATE cxx_std_17)

target_include_directories(base PUBLIC
  ${PROJECT_SOURCE_DIR}/libbase/include/
  ${PROJECT_SOURCE_DIR}/liblog/include/
)
