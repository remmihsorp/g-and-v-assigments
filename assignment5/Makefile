# Header Files
INCFLAGS = -I vecmath/include/

# Library Files
LINKFLAGS  = -lglut -lGL -lGLU 
Linkflags += -L vecmath/lib/ -lvecmath

CFLAGS = -O2 -Wall -Wextra
CC = g++

SRCS = $(wildcard *.cpp)
SRCS += $(wildcard vecmath/src/*.cpp)
OBJS = $(SRCS:.cpp=.o)
PROG = a5

all: $(PROG)

$(PROG): $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) -o $@ $(LINKFLAGS)
.cpp.o:
	$(CC) $(CFLAGS) $< -c -o $@ $(INCFLAGS)
clean:
	rm -f *.bak vecmath/src/*.o *.o core.* $(PROG) 
