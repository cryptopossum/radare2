BIN=rabin2
BINDEPS=r_magic r_core r_bin r_egg r_cons r_main
BINDEPS+=r_config r_io r_flag r_asm
BINDEPS+=r_debug r_hash r_lang r_anal r_parse r_bp r_reg
BINDEPS+=r_search r_syscall r_socket r_fs r_magic r_crypto r_util

include ../rules.mk

include ../../libr/socket/deps.mk
include ../../libr/main/deps.mk
include ../../shlr/zip/deps.mk
include ../../shlr/gdb/deps.mk
include ../../shlr/java/deps.mk
include ../../shlr/grub/deps.mk
include ../../shlr/bochs/deps.mk
include ../../shlr/qnx/deps.mk
include ../../shlr/ar/deps.mk
include ../../shlr/capstone.mk

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
LINKTO+=../../libr/bin/libr_bin.a
LINKTO+=../../libr/main/libr_main.a

wasi:
	$(CC) -flto -o rabin2.wasm rabin2.c -I ../../libr/include -I../../shlr/sdb/src $(LINKTO)
