CC = icc
CFLAGS = -qopt-report=5 -no-vec -qopenmp -xHost -Wall -Wextra

OBJSUM := $(patsubst %.c,%.o,$(wildcard src/*.c))
OBJSUMF := $(patsubst %.c,%.exec,$(wildcard src/*.c))

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $<

all: main.o dot
	@echo "Compiled!"

%.exec: %.o
	$(CC) $(CFLAGS) -o $@ $< main.o

dot: $(OBJSUMF)

clean:
	rm -rf main.o *.optrpt $(OBJSUM) $(OBJSUMF)