if(USE_TRANSFORMS)
  add_subdirectory(transforms)
  message(STATUS "Include Graph Transformations")
  set(Caffe2_CONTRIB_TRANSFORMS_CPU_SRC
    "${CMAKE_CURRENT_SOURCE_DIR}/transform.cc"
    "${CMAKE_CURRENT_SOURCE_DIR}/pattern_net_transform.cc"
    "${CMAKE_CURRENT_SOURCE_DIR}/graph.cc"
  )

  set(Caffe2_CPU_SRCS ${Caffe2_CPU_SRCS} ${Caffe2_TRANSFORMS_CPU_SRC})
  set(Caffe2_CPU_SRCS ${Caffe2_CPU_SRCS} PARENT_SCOPE)
endif()
