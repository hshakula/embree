## Copyright 2009-2020 Intel Corporation
## SPDX-License-Identifier: Apache-2.0

SET(libraries "")
IF (TASKING_INTERNAL)
  SET(public_class taskschedulerinternal)
ELSEIF (TASKING_TBB)
  ##############################################################
  # Find TBB
  ##############################################################
  if (NOT ${EMBREE_TBB_ROOT} STREQUAL "")
    set(TBB_ROOT ${EMBREE_TBB_ROOT})
  endif()
  FIND_PACKAGE(TBB REQUIRED tbb)

  ##############################################################
  # Create tasking target and link against TBB. Also set include directory
  # information on tasking target to provide the "algorithms" object library
  # with the TBB header files
  ##############################################################
  SET(public_class taskschedulertbb)
  SET(libraries TBB)
  SET(include_dirs "${TBB_INCLUDE_DIRS}")

  include(installTBB)

ELSEIF (TASKING_PPL)
  SET(public_class taskschedulerppl)
  SET(libraries ${PPL_LIBRARIES})
ENDIF()

ADD_COMMON_LIBRARY(tasking
    PUBLIC_CLASSES ${public_class}
    PUBLIC_HEADERS taskscheduler.h
    LIBRARIES ${libraries}
    INCLUDE_DIRS ${include_dirs})
