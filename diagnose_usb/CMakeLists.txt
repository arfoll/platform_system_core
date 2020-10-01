add_library(diagnose_usb SHARED
  diagnose_usb.cpp
)

target_include_directories(diagnose_usb PUBLIC
  ${PROJECT_SOURCE_DIR}/diagnose_usb/include/
  ${PROJECT_SOURCE_DIR}/libbase/include
)

target_compile_features(diagnose_usb PRIVATE cxx_std_17)
