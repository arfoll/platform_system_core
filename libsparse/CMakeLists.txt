find_package(ZLIB REQUIRED)

add_library(sparse SHARED
  backed_block.cpp
  output_file.cpp
  sparse.cpp
  sparse_crc32.cpp
  sparse_err.cpp
  sparse_read.cpp
)

target_include_directories(sparse PUBLIC ${PROJECT_SOURCE_DIR}/libsparse/include/
  ${PROJECT_SOURCE_DIR}/libbase/include/
)

set_target_properties(sparse PROPERTIES PUBLIC_HEADER include/sparse/sparse.h)

target_link_libraries(sparse ZLIB::ZLIB)
