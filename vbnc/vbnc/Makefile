thisdir = vbnc/vbnc
SUBDIRS =
include ../../build/rules.make

LOCAL_VBNC_FLAGS = @vbnc.exe.rsp

PROGRAM = $(topdir)/class/lib/vbnc/vbnc.exe
PROGRAM_COMPILE = $(BOOT_COMPILE)

include ../../build/executable.make

vbnc.exe.sources: vbnc.vbnc.rsp source/vbnc.vbproj
	MONO_PATH="../../class/lib/bootstrap:$MONO_PATH" mono ../../tools/extract-source/extract-source.exe -s:source/vbnc.vbproj -d:vbnc.exe.sources -m:l -b:source/ -x:r