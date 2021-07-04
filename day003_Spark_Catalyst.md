# Spark Catalyst 

#### Structured API
  * Declarative 
    * For example, calculate avg of a column without having to specify the programming steps to achieve that result.
  * Limited operations
  * Optimization possible due to a limited set of operations
  * However, we can accommodate vast majority of computations
  
   ![Spark Catalyst](https://github.com/fullstackdata/freshstart/blob/gh-pages/SparkCatalyst.png)
   
   Transformations
  ##### Query Plans 
  * Logical plans
    * Ex: Join
  * Physica Plans
    * can be executed
    * Ex: Sort-Merge join
