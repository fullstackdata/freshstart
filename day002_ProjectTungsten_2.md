# Project Tungsten
[Bringing Apache Spark performance closer to bare metal](https://databricks.com/blog/2015/04/28/project-tungsten-bringing-spark-closer-to-bare-metal.html)<br/>
Even though garbage collection in JVM is a very impressive engineering feat, the pressure of garbage collection is real.
Java objects have a huge overhead. A simple string with 4 Bytes takes a total of 48 Bytes in memory.
If object storage is compact, more objects can be stored in RAM and GC pressure can be relieved.
Also, Java is for general-purpose applications where as Spark's data flows are very well understood.

### Tungsten encoding 
* does not use Java Objects, <b>accesses binary data</b> directly
* utilizes <b>sun.misc.unsafe</b>, an advanced JVM functionality that exposes c-style memory access
* <b>intrinsic</b> each method call is compiled by JIT into a single machine instruction

### Cache Awareness
* In addition to in-memory performance gains, Spark can process data that is orders of magnitude higher than the memory capacity by<br/> efficient spilling of data to disk.
* Similarly, L1, L2, L3 CPU caches are orders of magnitude faster than main memory and Spark takes advantage of this by designing <br/> <b>cache friendly algorithms</b>.

### Code Generation
