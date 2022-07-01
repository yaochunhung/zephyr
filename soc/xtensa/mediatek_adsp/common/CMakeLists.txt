# MediaTek SoC family CMake file
#
# Copyright (c) 2022 MediaTek
# SPDX-License-Identifier: Apache-2.0

zephyr_interface_library_named(MEDIATEK_ADSP_COMMON)

zephyr_library_named(mediatek_adsp_common)
zephyr_library_include_directories(include)
zephyr_library_include_directories(${ZEPHYR_BASE}/drivers)

zephyr_library_sources(soc.c)

zephyr_library_link_libraries(MEDIATEK_ADSP_COMMON)

target_include_directories(MEDIATEK_ADSP_COMMON INTERFACE include)
target_link_libraries(MEDIATEK_ADSP_COMMON INTERFACE mediatek_adsp_common)
