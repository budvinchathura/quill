MPI and boost should be installed in the system before compiling.
Configure the AltMakefile with correct paths for boost and [sparsehash](https://github.com/sparsehash/sparsehash)

----
Compile with

```make -f AltMakefile```

----

Run command

```mpirun ./kmer_counter.out path/to/encoded.bin k_value path/to/output/folder/```

Example

```mpirun -np 16 --hostfile hostfile.txt kmer_counter.out vesca.fastq 28 ./test_results/data/```


----
----

Finalizer tool

Compile with

```make -f AltMakefile finalizer```

----

Run command

```mpirun ./finalizer.out k_value path/to/file_with_query_kmers no_of_queries_to_run path/to/output/folder```

Note: Use same number of processors for counter and finalizer. Use the same output folder path used for counting, except the trailing /

Example format of query kmer file (for `kmer_size`=5)


> AAAAA <br/> AAAAC <br/> ACGTT <br/> AAAAT <br/> TTTTG <br/> TTTTT

For example if `no_of_queries_to_run` = 5, then only the first 5 kmers will be queried for count.


