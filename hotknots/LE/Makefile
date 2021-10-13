CXX = g++
CXXFLAGS = -g -I./include -I../simfold/include -I../simfold/src/common -I../simfold/src/simfold -Wno-deprecated -Wno-write-strings -fPIC
LFLAGS = -lm -fPIC ../simfold/libsimfold.a

SOURCES = $(wildcard src/*.cpp)
OBJECTS = $(SOURCES:.cpp=.o)
TARGET = libpkenergy.so

$(TARGET): $(OBJECTS)
	$(CXX) -shared -o $@ $(OBJECTS) $(LFLAGS)

clean:
	rm -rf $(TARGET) $(OBJECTS)
