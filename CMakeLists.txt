cmake_minimum_required(VERSION 3.3)

project(mod_amd C)

set(FREESWITCH_INCLUDE_DIR "/usr/local/freeswitch/include/freeswitch" CACHE PATH "Location of FreeSWITCH headers")
set(INSTALL_MOD_DIR "/usr/local/freeswitch/mod" CACHE PATH "Location install library")

add_library(mod_amd SHARED mod_amd.c)
target_include_directories(mod_amd PRIVATE  ${FREESWITCH_INCLUDE_DIR} )

set_target_properties(mod_amd PROPERTIES PREFIX "")
set_target_properties(mod_amd PROPERTIES OUTPUT_NAME "mod_amd")

install(TARGETS mod_amd DESTINATION ${INSTALL_MOD_DIR})