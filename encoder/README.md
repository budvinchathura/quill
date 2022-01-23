MPI and boost should be installed in the system before compiling.
Configure the AltMakefile with correct paths for boost and [sparsehash](https://github.com/sparsehash/sparsehash)

----
Compile with

```make -f AltMakefile kmer_encoder```

----

Run command

```mpirun ./kmer_encoder.out path/to/datafile k_value path/to/output/folder/```

Example

```mpirun -np 16 --hostfile hostfile.txt kmer_encoder.out vesca.fastq 28 ./test_results/data/```

