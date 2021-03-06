cmake_minimum_required(VERSION 3.13.1)

include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(hello_world)

add_library(
	myLib
	src/lauxlib.c
	src/lauxlib.h
	src/lua.h
	src/lapi.c
	src/lapi.h
	src/lbaselib.c
	src/lcode.c
	src/lcode.h
	src/ldblib.c
	src/ldebug.c
	src/ldebug.h
	src/ldo.c
	src/ldo.h
	src/ldump.c
	src/lfunc.c
	src/lfunc.h
	src/lgc.c
	src/lgc.h
	src/linit.c
	src/liolib.c
	src/llex.c
	src/llex.h
	src/llimits.h
	src/lmathlib.c
	src/lmem.c
	src/lmem.h
	src/loadlib.c
	src/lobject.c
	src/lobject.h
	src/lopcodes.c
	src/lopcodes.h
	src/loslib.c
	src/lparser.c
	src/lparser.h
	src/lstate.c
	src/lstate.h
	src/lstring.c
	src/lstring.h
	src/lstrlib.c
	src/ltable.c
	src/ltable.h
	src/ltablib.c
	src/ltm.c
	src/ltm.h
	src/luaconf.h
	src/lualib.h
	src/lundump.c
	src/lundump.h
	src/lvm.c
	src/lvm.h
	src/lzio.c
	src/lzio.h
	src/lctype.c
	src/lctype.h
	src/lutf8lib.c
	src/lcorolib.c
	)

target_sources(app PRIVATE src/main.c)
target_link_libraries(app PRIVATE myLib)
