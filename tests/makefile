PROG_DIR = ../
CPPUTEST_HOME = cpputest


CXX = g++
CXXFLAGS  = -Wall -I$(PROG_DIR)
CXXFLAGS += -m32
CXXFLAGS += -I$(CPPUTEST_HOME)/include

##UNCOMMENT TO TEST MEMORY LEAK
#CXXFLAGS += -include $(CPPUTEST_HOME)/include/CppUTest/MemoryLeakDetectorNewMacros.h

LD_LIBRARIES = -L$(CPPUTEST_HOME)/lib -lCppUTest -lCppUTestExt

run: tests
	./tests
	
tests: *.cpp $(filter-out main.%, $(PROG_DIR)*.cpp)
	$(CXX) $(CXXFLAGS) $^ $(LD_LIBRARIES) -o tests
	
	

	
