## Copyright 2009-2020 Intel Corporation
## SPDX-License-Identifier: Apache-2.0

SET(libraries "")
IF (TASKING_INTERNAL)
  SET(public_class taskschedulerinternal)
ELSEIF (TASKING_TBB)
  SET(public_class taskschedulertbb)
  SET(libraries ${TBB_LIBRARIES})
ELSEIF (TASKING_PPL)
  SET(public_class taskschedulerppl)
  SET(libraries ${PPL_LIBRARIES})
ENDIF()

ADD_COMMON_LIBRARY(tasking
    PUBLIC_CLASSES ${public_class}
    PUBLIC_HEADERS taskscheduler.h
    LIBRARIES ${libraries})
