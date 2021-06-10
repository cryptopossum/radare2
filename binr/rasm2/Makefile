BIN=rasm2
BINDEPS=r_main

include ../../config-user.mk
include ../../libr/main/deps.mk
include ../../shlr/zip/deps.mk
include ../../shlr/java/deps.mk
include ../../shlr/capstone.mk
include ../rules.mk
LDFLAGS+=$(LINK)

LINKTO+=../../libr/util/libr_util.a
LINKTO+=../../libr/core/libr_core.a
LINKTO+=../../libr/magic/libr_magic.a
LINKTO+=../../libr/socket/libr_socket.a
LINKTO+=../../libr/debug/libr_debug.a
LINKTO+=../../libr/anal/libr_anal.a
LINKTO+=../../libr/reg/libr_reg.a
LINKTO+=../../libr/flag/libr_flag.a
LINKTO+=../../libr/search/libr_search.a
LINKTO+=../../libr/syscall/libr_syscall.a
LINKTO+=../../libr/bp/libr_bp.a
LINKTO+=../../libr/parse/libr_parse.a
LINKTO+=../../libr/asm/libr_asm.a
LINKTO+=../../libr/main/libr_main.a

wasi:
	$(CC) -flto -o rasm2.wasm rasm2.c -I ../../libr/include -I../../shlr/sdb/src $(LINKTO)
