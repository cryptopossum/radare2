BIN=rax2
BINDEPS=r_util r_main

include ../rules.mk
include ../../libr/main/deps.mk
include ../../shlr/zip/deps.mk
include ../../shlr/java/deps.mk
include ../../shlr/gdb/deps.mk

LDFLAGS+=$(LINK)

LINKTO+=../../libr/util/libr_util.a
LINKTO+=../../libr/main/libr_main.a

wasi:
	$(CC) -o rax2.wasm rax2.c -I ../../libr/include -I../../shlr/sdb/src $(LINKTO)
