PROJECT(infer_demo C CXX)
CMAKE_MINIMUM_REQUIRED (VERSION 3.10)

# specify the decompress directory of FastDeploy SDK
option(FASTDEPLOY_INSTALL_DIR "Path of downloaded fastdeploy sdk.")
include(${FASTDEPLOY_INSTALL_DIR}/utils/gflags.cmake)
include(${FASTDEPLOY_INSTALL_DIR}/FastDeploy.cmake)

include_directories(${FASTDEPLOY_INCS})

add_executable(benchmark_yolov5 ${PROJECT_SOURCE_DIR}/benchmark_yolov5.cc)
add_executable(benchmark_ppyolov5 ${PROJECT_SOURCE_DIR}/benchmark_ppyolov5.cc)
add_executable(benchmark_ppyolov6 ${PROJECT_SOURCE_DIR}/benchmark_ppyolov6.cc)
add_executable(benchmark_ppyolov7 ${PROJECT_SOURCE_DIR}/benchmark_ppyolov7.cc)
add_executable(benchmark_ppyolov8 ${PROJECT_SOURCE_DIR}/benchmark_ppyolov8.cc)
add_executable(benchmark_ppyolox ${PROJECT_SOURCE_DIR}/benchmark_ppyolox.cc)
add_executable(benchmark_ppyoloe ${PROJECT_SOURCE_DIR}/benchmark_ppyoloe.cc)
add_executable(benchmark_picodet ${PROJECT_SOURCE_DIR}/benchmark_picodet.cc)
add_executable(benchmark_ppcls ${PROJECT_SOURCE_DIR}/benchmark_ppcls.cc)
add_executable(benchmark_ppseg ${PROJECT_SOURCE_DIR}/benchmark_ppseg.cc)
add_executable(benchmark_ppmatting ${PROJECT_SOURCE_DIR}/benchmark_ppmatting.cc)
add_executable(benchmark_ppocr_det ${PROJECT_SOURCE_DIR}/benchmark_ppocr_det.cc)
add_executable(benchmark_ppocr_cls ${PROJECT_SOURCE_DIR}/benchmark_ppocr_cls.cc)
add_executable(benchmark_ppocr_rec ${PROJECT_SOURCE_DIR}/benchmark_ppocr_rec.cc)

if(UNIX AND (NOT APPLE) AND (NOT ANDROID))
  target_link_libraries(benchmark_yolov5 ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppyolov5 ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppyolov6 ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppyolov7 ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppyolov8 ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppyolox ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppyoloe ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_picodet ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppcls ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppseg ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppmatting ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppocr_det ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppocr_cls ${FASTDEPLOY_LIBS} gflags pthread)
  target_link_libraries(benchmark_ppocr_rec ${FASTDEPLOY_LIBS} gflags pthread)
else()
  target_link_libraries(benchmark_yolov5 ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppyolov5 ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppyolov6 ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppyolov7 ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppyolov8 ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppyolox ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppyoloe ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_picodet ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppcls ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppseg ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppmatting ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppocr_det ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppocr_cls ${FASTDEPLOY_LIBS} gflags)
  target_link_libraries(benchmark_ppocr_rec ${FASTDEPLOY_LIBS} gflags)
endif()
# only for Android ADB test
if(ANDROID)
  install_fastdeploy_libraries(${CMAKE_CURRENT_BINARY_DIR})
endif()
