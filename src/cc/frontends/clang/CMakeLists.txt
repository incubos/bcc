# Copyright (c) PLUMgrid, Inc.
# Licensed under the Apache License, Version 2.0 (the "License")

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -DKERNEL_MODULES_DIR='\"${BCC_KERNEL_MODULES_DIR}\"'")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -DKERNEL_MODULES_SUFFIX='\"${BCC_KERNEL_MODULES_SUFFIX}\"'")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -DKERNEL_HAS_SOURCE_DIR=${BCC_KERNEL_HAS_SOURCE_DIR}")
add_library(clang_frontend loader.cc b_frontend_action.cc tp_frontend_action.cc kbuild_helper.cc)
