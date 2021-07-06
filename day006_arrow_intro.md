# Arrow
Arrow is an open, in-memory columnar data format for <b>flat</b> and <b>hierarchical</b> data.
Arrow is designed for efficient analytic operations on modern hardware like CPUs and GPUs.
With its many libraries, connectors and bindings, Arrow is the defacto format for many modern languages (adoption by 11 languages), frameworks, databases and tools.
Arrow achieves its efficiency by using SIMD instructions.

##### Sources of waste
* Serialization, deserialization
* Transport protocols
* Transport glue code

To reduce the overhead of serialization and deserialization, some standards have to be developed and well adopted.<br/>
There is a network effect in how useful a standard can be. Adoption builds more adoption.

Arrow is in-memory, but confusingly enough for beginners, there are arrow files. These are meant to be for inter-process communication.




