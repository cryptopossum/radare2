BIN=rafind2

BINDEPS=r_search r_io r_asm r_anal r_reg r_cons r_lang r_crypto
BINDEPS+=r_socket r_parse r_util r_syscall r_flag r_hash r_main

include ../rules.mk

include ../../libr/socket/deps.mk
include ../../libr/main/deps.mk
include ../../shlr/zip/deps.mk
include ../../shlr/gdb/deps.mk
include ../../shlr/bochs/deps.mk
include ../../shlr/qnx/deps.mk
include ../../shlr/ar/deps.mk

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
LINKTO+=../../libr/io/libr_io.a
LINKTO+=../../libr/cons/libr_cons.a
LINKTO+=../../libr/main/libr_main.a

wasi:
	$(CC) -flto -o rafind2.wasm rafind2.c -I ../../libr/include -I../../shlr/sdb/src $(LINKTO)
