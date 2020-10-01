add_definitions(-DZLIB_CONST)

find_package(ZLIB REQUIRED)

add_library(ziparchive SHARED
  zip_archive.cc
  zip_archive_stream_entry.cc
  zip_cd_entry_map.cc
  zip_error.cpp
  zip_writer.cc
)

target_include_directories(ziparchive PUBLIC
  ${PROJECT_SOURCE_DIR}/libbase/include/
  ${PROJECT_SOURCE_DIR}/libziparchive/include
  ${PROJECT_SOURCE_DIR}/liblog/include
)

target_link_libraries(ziparchive ZLIB::ZLIB)
target_compile_features(ziparchive PRIVATE cxx_std_17)

