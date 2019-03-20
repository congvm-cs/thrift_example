# g++ -DHAVE_INTTYPES_H -DHAVE_NETINET_IN_H -Wall 
# -I/usr/local/include/thrift 
# *.cpp 
# -L/usr/local/lib 
# -lthrift -lthriftnb -levent -lssl -lcrypto 
# -o server


CC = g++
CFLAGS = -std=c++11 -g -Wall -D_DEBUG -Wshadow -Wno-sign-compare -w

DIR = ../gen-cpp/

INC = -I/usr/local/include/thrift
INC += -I./include/third_party
INC += -I./include
INC += -I./include/nsync/public/

LDFLAGS =  -lthrift -lthriftnb -levent -lssl -lcrypto 
LDFLAGS += -L/usr/local/lib 

all: server

server:
	$(CC) $(CFLAGS) -o server *.cpp $(INC) $(LDFLAGS)