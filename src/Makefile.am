bin_PROGRAMS = driver

driver_SOURCES = \
  main.cpp

driver_LDADD = ../libblsct.a ../libbls384_256.a ../libmcl.a
driver_CXXFLAGS = -Wall -std=c++17 
driver_CPPFLAGS = -I../include -I../navcoin/src -I../../navcoin/src/bls/include -I../../navcoin/src/bls/mcl/include -I../../navcoin/src/blsct/external_api
	
if OS_DARWIN
driver_LDFLAGS = -Wl,-dead_strip
else
driver_LDFLAGS = -Wl,-z,relro -Wl,-z,now -Wl,-z,separate-code -pie -pthread
endif
