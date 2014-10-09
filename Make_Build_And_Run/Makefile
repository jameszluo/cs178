#!/usr/bin/make
# Author: James Luo
# Date: 9/17/2014
# CS 178
# Make_Build_And_Run
############################################################

countThrees : countThrees.o readInt32BitLE.o
	gcc -o countThrees countThrees.o readInt32BitLE.o

countThrees.o : countThrees.c readInt32BitLE.h
	gcc -c countThrees.c
readInt32BitLE.o : readInt32BitLE.c readInt32BitLE.h
	gcc -c readInt32BitLE.c
test : countThrees
	./countThrees
clean :
	rm -f countThrees countThrees.o readInt32BitLE.o
