NEED_GTEST_WITH_MAIN := 1
NEED_GFLAGS := 1

include /usr/local/gtest/Makefile.env
include /usr/local/gflags/Makefile.env

SRC := $(wildcard *.cc)
OBJ := $(patsubst %.cc,%.o,${SRC})
TARGET := libgtestx.a

CXX := /data/gcc-build-4.8.1/bin/g++
CXXFLAGS += -fPIC -shared -std=c++0x -O2 -g
CXXFLAGS += -I..

.PHONY: all clean

all: ${TARGET}

${TARGET}: %: ${OBJ}
	${AR} ${ARFLAGS} $@ $^

${OBJ}: %.o: %.cc
	${CXX} ${CXXFLAGS} -c -o $@ $<

clean:
	${RM} ${TARGET} ${OBJ}
