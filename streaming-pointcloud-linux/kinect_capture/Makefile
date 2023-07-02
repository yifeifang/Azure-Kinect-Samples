include define.inc
CFLAGS += -I./kinect_capture/include -std=c++17
SRCDIR:=./kinect_capture/src
BUILDDIR:=$(BUILD)/kinect_capture
SOURCES:=$(wildcard $(SRCDIR)/*.cpp)  # this finds all the C source files under the source directory
OBJECTS:=$(patsubst $(SRCDIR)/%.cpp,$(BUILDDIR)/%.o,$(SOURCES))  # this maps each source file to its corresponding object file
$(info $$SOURCES is [${SOURCES}])
$(info $$OBJECTS is [${OBJECTS}])

$(BUILDDIR)/%.o: $(SRCDIR)/%.cpp  # this defines a pattern rule for each object file
	$(CC) $(CFLAGS) -c $< -o $@  # this compiles the source file ($<) to the object file ($@)

.PHONY compile: $(OBJECTS)  # this defines the all target that depends on all the object files

.PHONY link: compile

.PHONY all: link
