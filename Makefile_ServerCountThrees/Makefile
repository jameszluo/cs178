#!/usr/bin/make
# Author: James Luo
# Date: 9/25/2014
# CS 178
# Makefile_ServerCountThrees
############################################################

ServerCountThrees : ServerCountThrees.o readInt32BitLE.o
	gcc -o ServerCountThrees ServerCountThrees.o readInt32BitLE.o

ServerCountThrees.c readInt32BitLE.c readInt32BitLE.h : ServerCountThrees.zip
	unzip ServerCountThrees.zip
	touch ServerCountThrees.c readInt32BitLE.c readInt32BitLE.h
ServerCountThrees.o : ServerCountThrees.c readInt32BitLE.h
	gcc -c ServerCountThrees.c
readInt32BitLE.o : readInt32BitLE.c readInt32BitLE.h
	gcc -c readInt32BitLE.c
test : ServerCountThrees threesData.bin
	./ServerCountThrees
threesData.bin : threesData.zip
	unzip threesData.zip
	touch threesData.bin

.PHONY : clean
clean :
	rm -f ServerCountThrees ServerCountThrees.[co] readInt32BitLE.[cho] \
            threesData.bin
