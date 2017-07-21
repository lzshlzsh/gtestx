NEED_GTEST := 1
NEED_GFLAGS := 1

include /usr/local/gtest/Makefile.env
include /usr/local/gflags/Makefile.env

CXX := /data/gcc-build-4.8.1/bin/g++
CXXFLAGS += -Wall -I../src -std=c++0x
LDFLAGS += -pthread -Wl,-dn $(addprefix -l,stdc++) -Wl,-dy
LDFLAGS += -L../src/gtestx -lgtestx

all: gtestx_examples

gtestx_examples: $(wildcard *.cc)
	${CXX} ${CXXFLAGS} -o $@ $^ ${LDFLAGS}

clean:
	rm -f gtestx_examples

.PHONY: all clean
