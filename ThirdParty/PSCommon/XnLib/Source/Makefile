include ../../BuildSystem/CommonDefs.mak

BIN_DIR = ../Bin

INC_DIRS = \
	../Include \
	/usr/local/include

SRC_FILES = \
	*.cpp \
	Linux/*.cpp

ifeq ("$(OSTYPE)","Darwin")
	INC_DIRS += /opt/local/include
	LIB_DIRS += /opt/local/lib
	LDFLAGS += -framework CoreFoundation -framework IOKit
endif

SLIB_NAME = XnLib
USED_LIBS = usb-1.0 dl pthread udev
ifneq ("$(OSTYPE)","Darwin")
	USED_LIBS += rt 
endif
CFLAGS += -Wall

include ../../BuildSystem/CommonCppMakefile
