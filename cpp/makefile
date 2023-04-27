THRIFT_VER =thrift-0.19.0
INCS_DIRS  =-I/usr/local/include/thrift/
LIBS_DIRS  =-L/usr/local/lib/
CPP_DEFS   =-D=HAVE_CONFIG_H
CPP_OPTS   =-Wall -O2
LIBS       =-lthrift

GEN_SRC    = ../gen-cpp/SharedService.cpp  \
             ../gen-cpp/shared_types.cpp   \
             ../gen-cpp/tutorial_types.cpp \
             ../gen-cpp/Calculator.cpp
GEN_INC    = -I../gen-cpp

default: server client

server: CppServer.cpp
	g++ ${CPP_OPTS} ${CPP_DEFS} -o CppServer ${GEN_INC} ${INCS_DIRS} CppServer.cpp ${GEN_SRC} ${LIBS_DIRS} ${LIBS}

client: CppClient.cpp
	g++ ${CPP_OPTS} ${CPP_DEFS} -o CppClient ${GEN_INC} ${INCS_DIRS} CppClient.cpp ${GEN_SRC} ${LIBS_DIRS} ${LIBS}

clean:
	$(RM) -r CppClient CppServer
