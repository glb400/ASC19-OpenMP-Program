TARGET=FYArray.exe

CXX=icpc
CXXFLAGS= -qopenmp -xHost -qopt-report-phase=vec -O3
LDFLAGS= -qopenmp -xHost -qopt-report-phase=vec -O3

INCLUDE=../include

OBJ=FYStorage.o main.o

$(TARGET):$(OBJ)
	$(CXX) $(LDFLAGS) $^ -o $@ 
	cp $(TARGET) ../
	

%.o:%.cpp
	$(CXX) $(CXXFLAGS) -I$(INCLUDE) -c $< -o $@ 

.PHONY:clean
clean:
	rm *.o -f
