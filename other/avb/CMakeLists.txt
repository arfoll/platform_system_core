add_definitions(-DAVB_COMPILATION)

add_library(avb SHARED
 avb_chain_partition_descriptor.c
 avb_cmdline.c
 avb_crc32.c
 avb_crypto.c
 avb_descriptor.c
 avb_footer.c
 avb_hash_descriptor.c
 avb_hashtree_descriptor.c
 avb_kernel_cmdline_descriptor.c
 avb_property_descriptor.c
 avb_rsa.c
 avb_sha256.c
 avb_sha512.c
 avb_slot_verify.c
 avb_util.c
 avb_vbmeta_image.c
 avb_version.c
 avb_sysdeps_posix.c
)

#target_include_directories(avb PUBLIC ${PROJECT_SOURCE_DIR}/libsparse/include/)

#set_target_properties(sparse PROPERTIES PUBLIC_HEADER include/sparse/sparse.h)

##target_link_libraries(sparse ZLIB::ZLIB)
