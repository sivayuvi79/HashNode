# Hive SerDe

# Hive SerDe

Hive uses SerDe and File format for IO operations on HDFS.

**Serialization** -> Converting Java Objects into bytes(String or Binary data)

**De-serialization** ->Converting bytes into Java Objects.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666110305414/6qOKvmU1S.png align="left")

Hive uses inbuilt library for this kind of operation, In this library we have so many methods for different different file formats.
Built-in SerDes are Avro, ORC, RegEx, Parquet, CSV, JsonSerDe, etc.

We can also create our own Serde and assign some properties over there.

lets take an example, I want to store csv file and in this file I have column which may have following kind of data **Hi, Siva. How are you?. Do you know "SerDe"**. In this text we have comma which is used as separator in csv file and double quote which is used as quoted string in csv files. So our raw text should be like below,
**"Hi, Siva. How are you?. Do you know \"SerDe\""**. 

To do this we have some properties in CSV SerDe library. Those properties need to be applied while creating a table.

