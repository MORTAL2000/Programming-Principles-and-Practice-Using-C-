CC=g++-4.9
CFLAGS=-std=c++14 -lbookgui `fltk-config --cxxflags --ldflags` -lfltk_images -lfltk_gl -lfltk_forms -lfltk -ljpeg -Wno-narrowing
AR = ar
SOURCES = $(shell ls *.cpp)
OBJECTS = ${SOURCES:.cpp=.o}
TARGETS = lib13.a
DEPS = 13.h

all: $(TARGETS)

%.a: $(OBJECTS)
	$(AR) rcs $@ $(OBJECTS)

%.o: %.cpp $(DEPS)
	$(CC) $(CFLAGS) -o $@ -c $<

clean:	
	rm -rf $(OBJECTS) *.out *.stackdump



