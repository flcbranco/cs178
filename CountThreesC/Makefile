#!/usr/bin/make -f
# Name: Fabio Castello Branco
# Course: CS178 Build Automation for DevOps and QA
# CRN: 76718
# Date: 9/1/2018
# Assignment: CountThrees Makefile

SHELL = /bin/sh
#### Start of system configuration section. ####
srcdir = .
#### End of system configuration section. ####

# Professor Brown - Is it countThrees.c or Count3s.c?
#SRCS_C  = readInt32BitLE.h readInt32BitLE.c countThrees.c
SRCS_C  = $(wildcard *.c)
OBJS    = $(SRCS_C:.c=.o)

compile : $(SRCS_C)
	cc -c $(SRCS_C)

.PHONY: Count3s
Count3s : $(OBJS)
	cc -o Count3s $(OBJS)

runCount3s : Count3s
	./Count3s

.PHONY: clean
clean :
	rm -f $(OBJS) Count3s core
