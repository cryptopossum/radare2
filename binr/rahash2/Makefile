BIN=rahash2

BINDEPS=r_main

include ../rules.mk

ifeq ($(OSTYPE),android)
LDFLAGS+=-lm
endif

include ../../libr/socket/deps.mk
include ../../libr/main/deps.mk
include ../../shlr/zip/deps.mk
include ../../shlr/gdb/deps.mk
include ../../shlr/bochs/deps.mk
include ../../shlr/qnx/deps.mk
include ../../shlr/zip/deps.mk
include ../../shlr/ar/deps.mk

LDFLAGS+=$(LINK)

LINKTO+=../../libr/util/libr_util.a
LINKTO+=../../libr/main/libr_main.a
LINKTO+=../../libr/io/libr_io.a
LINKTO+=../../libr/hash/libr_hash.a
LINKTO+=../../libr/crypto/libr_crypto.a

wasi:
	$(CC) -o rahash2.wasm rahash2.c -I ../../libr/include -I../../shlr/sdb/src $(LINKTO)
