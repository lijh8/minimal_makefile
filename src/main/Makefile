# build dynamic library with -fPIC -shared
CFLAGS   = -g # -O3 -fPIC # CXXFLAGS for .cpp
CPPFLAGS = -MMD -MP # -I../foo -DNDEBUG
LDFLAGS  = # -L../foo -shared -static
LDLIBS   = # -lfoo
#CC      = $(CXX) # link with CXX for .cpp

# target name is basename of one of the source files
main: $(patsubst %.c,%.o,$(wildcard *.c)) # .cpp
-include *.d
clean: ; rm -fr *.o *.d main
.PHONY: clean
