# SPDX-License-Identifier: MIT
#
# Copyright (C) 2004 - 2022 AJA Video Systems, Inc.
#

DIR := $(strip $(shell dirname $(abspath $(lastword $(MAKEFILE_LIST)))))

ifeq (,$(filter _%,$(notdir $(CURDIR))))
  include $(DIR)/../../../../build/targets.mk
else
include $(DIR)/../../../../build/configure.mk

AJA_APP = $(A_UBER_BIN)/ntv2encodehevcvif

VPATH	 = $(A_DEMOAPPS_PATH)
INCLUDES = -I$(A_DEMOAPPS_PATH) -I$(A_LIB_NTV2_M31_PATH)

SRCS = main.cpp ntv2encodehevcvif.cpp ntv2encodehevcvifac.cpp ntv2demohevccommon.cpp

INCS = ntv2encodehevcvif.h ntv2encodehevcvifac.h ntv2demohevccommon.h

include $(DIR)/../../../../build/common.mk

endif

