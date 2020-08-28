## Copyright 2009-2020 Intel Corporation
## SPDX-License-Identifier: Apache-2.0

# ideally we would use target_link_libraries to provide the algorithms target
# with the TBB include directory information. Howeve, this is only possible in
# very recent versions of TBB and therefore we use the target property instead
GET_TARGET_PROPERTY(tasking_include_dirs tasking INCLUDE_DIRECTORIES)

ADD_COMMON_LIBRARY(algorithms
  PUBLIC_CLASSES
    parallel_filter
    parallel_for
    parallel_for_for
    parallel_for_for_prefix_sum
    parallel_map
    parallel_partition
    parallel_prefix_sum
    parallel_reduce
    parallel_set
    parallel_sort
  PUBLIC_HEADERS
    parallel_any_of.h
  INCLUDE_DIRS
    ${tasking_include_dirs})
