# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.13.1)
include_directories("./src")

find_package(Zephyr HINTS $ENV{ZEPHYR_BASE})
project(bluetooth_ctrl_user_ext)

zephyr_library_include_directories(${ZEPHYR_BASE}/subsys/bluetooth/controller/)

FILE(GLOB app_sources src/*.c)

target_sources(app PRIVATE ${app_sources})
