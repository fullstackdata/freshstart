# Vaex
* What is it
	* dataframe with state
* Where is it useful
	* to run notebooks on huge datasets on a laptop or a single node
* Why is it appealing
	* Familiar Pandas API
	* Familiar scikit-learn API
	* 10-1000x speedup over Pandas strings
	
## Overview
* vaex df = df + state
* state is similar to Spark RDD's DAG lineage (applying filters or other operations)
* state enables lazy evaluation
* lazy expressions are saved as virtual columns
* expression system 
	* allows jitting (numba, pythran, CUDA) 
	* memory efficient
* storage = hdf5 + arrow spec + memory mapping
* free pipelines

## Domain specific libraries for
* hdf5
* arrow
* viz
* server
* ml

###### Reference:
https://www.youtube.com/watch?v=ELtjRdPT8is
