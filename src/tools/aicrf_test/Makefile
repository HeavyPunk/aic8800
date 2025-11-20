#CROSS_COMPILE := /opt/toolchains/mips-gcc540-glibc222-64bit-r3.3.0/bin/mips-linux-gnu-

LDFLAGS := -lpthread

default: all

all: bt_test

bt_test: bt_test.o
	$(CROSS_COMPILE)gcc $+ $(LDFLAGS) -o $@

%.o: %.c
	$(CROSS_COMPILE)gcc -c $+ -o $@

clean:
	rm *.o bt_test

install:
	sudo cp bt_test /sbin