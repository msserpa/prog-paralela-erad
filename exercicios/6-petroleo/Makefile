CC=icc
CFLAGS=-no-vec -qopenmp -qopt-report=5 -Wall -Wextra -xHost

all: 6-petroleo.exec

6-petroleo.exec: prog_aux_3D.o 6-kernel.o prog_kernel_3D.o prog_MOD3D_testKERNEL.o
	$(CC) $^ -o $@ $(CFLAGS)

clean:
	rm -f *.bin *.txt *.o *.optrpt *.exec