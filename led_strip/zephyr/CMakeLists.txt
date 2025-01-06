cmake_minimum_required(VERSION 3.20.5)
set(DTC_OVERLAY_FILE "disco_f407vg.overlay")
include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(Switchboard)
FILE(GLOB app_sources ../src/*.c*)
target_sources(app PRIVATE ${app_sources})

