## Copyright 2009-2020 Intel Corporation
## SPDX-License-Identifier: Apache-2.0

ADD_COMMON_LIBRARY(simd
  PUBLIC_CLASSES
    sse
  PUBLIC_HEADERS
    avx.h
    avx512.h
    simd.h
    varying.h
    vboold4_avx.h
    vboold4_avx512.h
    vboold8_avx512.h
    vboolf16_avx512.h
    vboolf4_avx512.h
    vboolf4_sse2.h
    vboolf8_avx.h
    vboolf8_avx512.h
    vdouble4_avx.h
    vdouble8_avx512.h
    vfloat16_avx512.h
    vfloat4_sse2.h
    vfloat8_avx.h
    vint16_avx512.h
    vint4_sse2.h
    vint8_avx.h
    vint8_avx2.h
    vllong4_avx2.h
    vllong8_avx512.h
    vuint16_avx512.h
    vuint4_sse2.h
    vuint8_avx.h
    vuint8_avx2.h)
