## Copyright 2009-2020 Intel Corporation
## SPDX-License-Identifier: Apache-2.0

SET(CMAKE_THREAD_PREFER_PTHREAD TRUE)
FIND_PACKAGE(Threads REQUIRED)

ADD_COMMON_LIBRARY(sys
  PUBLIC_CLASSES
    alloc
    barrier
    condition
    filename
    library
    mutex
    regression
    string
    sysinfo
    thread
  PUBLIC_HEADERS
    array.h
    atomic.h
    intrinsics.h
    platform.h
    ref.h
    vector.h
  LIBRARIES
    ${CMAKE_THREAD_LIBS_INIT}
    ${CMAKE_DL_LIBS}
)
