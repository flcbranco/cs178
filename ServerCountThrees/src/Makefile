#!/usr/bin/make -f
#Name: Fabio Castello Branco
#Course: CS178 Build Automation for DevOps and QA
#CRN: 76718
#Date: 9/9/2018
#Assignment: 03 XLab: Makefile - Build and Launch ServerCountThrees

# ASSUMPTION: The make command is executed within the src directory
SHELL = /bin/sh

#### Start of system configuration section. ####
srcdir = .
datadir = ../data
builddir = ../build
#### End of system configuration section. ####
CC = gcc
INC_PATH = $(srcdir)
CFLAGS = -w -I$(INC_PATH)

SRCS_C  = readInt32BitLE.c ServerCountThrees.c
SOURCES=$(addprefix $(srcdir)/,$(SRCS_C))
EXECUTABLE=ServerCountThrees

.PHONY: test
test : build
	cp -pf $(datadir)/threesData.bin $(builddir)
	cp -pf $(srcdir)/$(EXECUTABLE) $(builddir)
	$(builddir)/$(EXECUTABLE)

.PHONY: build
build : clean $(builddir)
	$(CC) $(CFLAGS) -o $(EXECUTABLE) $(SOURCES)

$(builddir) :
	mkdir -pv $(builddir)

.PHONY: clean
clean :
	rm -rf $(builddir) $(EXECUTABLE) core
