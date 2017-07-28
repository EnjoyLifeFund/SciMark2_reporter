.SUFFIXES: .c .o

.c.o:
	$(CC) $(CFLAGS) $(DEBUGFLAG) -c -Ofast  -flto  $<

all: scimark2 

# CC = /usr/bin/cc

OBJS = FFT.o kernel.o Stopwatch.o Random.o SOR.o SparseCompRow.o array.o MonteCarlo.o LU.o 

scimark2 : scimark2.o $(OBJS)
	$(CC) $(CFLAGS) -o scimark2 scimark2.o $(OBJS) $(LDFLAGS) -lm

clean:
	rm $(OBJS) scimark2
