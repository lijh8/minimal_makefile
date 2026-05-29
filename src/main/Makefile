# build dynamic library with -fPIC -shared
CFLAGS   = -g # -O3 -fPIC
CXXFLAGS = -g # -O3 -fPIC
CPPFLAGS = -MMD -MP # -I../foo -DNDEBUG
LDFLAGS  = # -L../foo -shared -static
LDLIBS   = # -lfoo

ifeq ($(wildcard *.c),)
CC       = $(CXX) # link with CXX for .cpp
endif

# target name is basename of one of the source files
main: $(addsuffix .o,$(basename $(wildcard *.c *.cpp)))
-include *.d
clean: ; rm -fr *.o *.d main
.PHONY: clean
