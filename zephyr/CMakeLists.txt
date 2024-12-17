cmake_minimum_required(VERSION 3.20.1)

set(DTC_OVERLAY_FILE "stm32c031xx.overlay")
include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(Software)
FILE(GLOB app_sources ../src/*.c*)
target_sources(app PRIVATE ${app_sources})
zephyr_library_sources(ws2812/ws2812_gpio.c)
