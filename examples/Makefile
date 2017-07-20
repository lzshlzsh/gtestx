all: gtestx_examples

# change to your gtest source directory
GTEST_SRC_DIR = /home/lzs/github/googletest/googletest
GFLAGS_DIR := /usr/local/gflags

CXX := /data/gcc-build-4.8.1/bin/g++

gtestx_examples: $(wildcard *.cc) ../src/gtestx/gtestx.cc $(GTEST_SRC_DIR)/src/gtest-all.cc
	${CXX} -Wall -std=c++0x -I../src -I$(GTEST_SRC_DIR)/include -I$(GTEST_SRC_DIR) -I${GFLAGS_DIR}/include -o $@ $^ -pthread -L${GFLAGS_DIR}/lib -lgflags -Wl,-dn $(addprefix -l,stdc++) -Wl,-dy

clean:
	rm -f gtestx_examples

.PHONY: all clean
