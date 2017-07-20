all: gtestx_test

# change to your gtest source directory
GTEST_SRC_DIR = /home/lzs/github/googletest/googletest
GFLAGS_DIR := /usr/local/gflags

gtestx_test: gtestx_test.cc ../src/gtestx/gtestx.cc $(GTEST_SRC_DIR)/src/gtest-all.cc
	g++ -Wall -std=c++0x -I../src -I$(GTEST_SRC_DIR)/include -I$(GTEST_SRC_DIR) -I${GFLAGS_DIR}/include -o $@ $^ -pthread -L${GFLAGS_DIR}/lib -lgflags

clean:
	rm -f gtestx_test

.PHONY: all clean
