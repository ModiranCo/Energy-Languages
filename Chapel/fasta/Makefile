compile:
	cp fasta.chapel-2.chapel fasta.chapel-2.chpl
	/usr/local/src/chapel-1.15.0/bin/linux64/chpl --fast fasta.chapel-2.chpl -o fasta.chapel-2.chapel_run
measure:
	sudo ../../RAPL/main "./fasta.chapel-2.chapel_run --n=25000000" Chapel fasta

run:
	./fasta.chapel-2.chapel_run --n=25000000

mem:
	/usr/bin/time -v ./fasta.chapel-2.chapel_run --n=25000000

valgrind:
	valgrind --tool=massif --stacks=yes ./fasta.chapel-2.chapel_run --n=25000000
