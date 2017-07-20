NEED_GTEST_WITH_MAIN := 1
NEED_GFLAGS := 1

include /usr/local/gtest/Makefile.env
include /usr/local/gflags/Makefile.env

CXX := /data/gcc-build-4.8.1/bin/g++
CXXFLAGS += -Wall -I../src -std=c++0x
LDFLAGS += -pthread

all: gtestx_examples

gtestx_examples: $(wildcard *.cc) ../src/gtestx/gtestx.cc
	${CXX} ${CXXFLAGS} -o $@ $^ ${LDFLAGS}

clean:
	rm -f gtestx_examples

.PHONY: all clean
