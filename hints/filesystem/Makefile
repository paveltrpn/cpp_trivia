
CC := g++
CFLAGS := -IE:\Devtools\fmt-7.1.3\include -std=c++2a -O0
LFLAGS := -LE:\Devtools\fmt-7.1.3\build -lfmt

SRCS := $(wildcard *.cpp)
OBJS := $(SRCS:.cpp=.o)

VPATH := .

.phony: all clean

all: main

main.o: main.cpp
	$(CC) $(CFLAGS) -c $< -o $@

file.o: file.cpp
	$(CC) $(CFLAGS) -c $< -o $@

string_mnp.o: string_mnp.cpp common.h
	$(CC) $(CFLAGS) -c $< -o $@

main: $(OBJS)
	$(CC) $(OBJS) $(LFLAGS) -o $@ -lstdc++

clean:
	rm -f *.o main.exe
