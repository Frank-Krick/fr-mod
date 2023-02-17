include(../../3rdparty/max-sdk-base/script/max-pretarget.cmake)

add_library(${PROJECT_NAME} MODULE
  fr-tbp~.cpp)

target_include_directories(${PROJECT_NAME}
  PRIVATE fr_tbp
  PRIVATE "${MAX_SDK_INCLUDES}"
  PRIVATE "${MAX_SDK_MSP_INCLUDES}"
  PRIVATE "${MAX_SDK_JIT_INCLUDES}")

target_link_libraries(${PROJECT_NAME} PRIVATE fr_tbp)

include(../../3rdparty/max-sdk-base/script/max-posttarget.cmake)

set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 20)
set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD_REQUIRED ON)
