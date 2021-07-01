DataFrames are compiled down to logical plans.<br/>
Python, R or any other new language can create a wrapper to the DataFrame API. <br/>
Before DataFrames, UDFs written for RDDs were completely opaque to Spark, hence there was little room for optimizations. <br/>
From 2010 to 2015, **storage** and **networking** speeds increased ten-fold where as CPU processing speeds barely increased.<br/>
So **Project Tungsten** is a step to address this issue and make Spark performant by squeezing out CPU performance. <br/>
Not just for improving CPU performance, dataframes also help in abstracting away for other newer compilation developments with LLVM, GPUs, NVRAM etc. <br/>

# Tungsten
* Runtime code generation, that's close in performance to handwritten c++ code.
* Exploiting cache locality
* Off-heap memory management
