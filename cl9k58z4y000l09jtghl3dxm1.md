# Hive Partition

# Hive Partition
For efficient data analysis and loading we need partition in Hive, not only hive partition concept can be applicable in all other data platforms.

In Hive we can load only structured data, in that we can choose partitions in available columns, that columns can be chosen by below criteria,

- Should not be Primary key like column,
- It should be less uniqueness,
- frequently used column for filter.

There are two type of partition method available in Hive,

## Static Partition
In static partition we can specify the partition value while loading and so it will be little bit faster.

## Dynamic Partition
Here hive will find the distinct values for partition from partition column.

Hive support multi level partitions too. 


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666456538275/jjIL3b0ge.png align="left")
