SRC=main.cpp
CC=g++
PROFILE_FLAG=-pg 

ifeq ($(VERSION), DEBUG)
	VERSION_FLAGS=$(DEBUG_FLAGS)
else
	VERSION_FLAGS=$(RELEASE_FLAGS)
	OPT=-O2
endif

CFLAGS=-Wall -W -Werror -g -std=c++0x $(VERSION_FLAGS) #-DBASE_THRESHOLD=10
LIB=-L/usr/local/lib/ 

main: $(SRC)
	$(CC) $(CFLAGS) $(OPT) $^ -o $@

print_vars:
	-echo ${VERSION}

clean:
	-rm main
