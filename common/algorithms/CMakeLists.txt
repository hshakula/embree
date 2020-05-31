## Copyright 2009-2020 Intel Corporation
## SPDX-License-Identifier: Apache-2.0

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
    parallel_any_of.h)
