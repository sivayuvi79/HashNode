# Why DBMS instead of Traditional file system?

# Why DBMS instead of File system?

File system will not be efficient for long run and frequent changes. File System useful only when need of bulk dump or temporary storage.

# Advantages of DBMS over file system


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666283520304/sdJ22vWCZ.png align="left")
 
**1. Querying:**
  DMBS uses indexing concept so we can query the data with help of predefined algorithms like Binary tree search and Hashing.

**2. Data redundancy:**
No need of storing same kind of data like customer address can be stored in single table and we can use it further with help of table join.

**3. Consistency:**
If any customer changes the address we just update the customer table alone and it will be automatically picked up while joining.

**4. Data Independence:**
Hides the low level information like where it is stored, how it is stored and when it is loaded. Engineers not need to worry about this details.

**5. Security:**
Critical Data can be locked for particular users and some data available only to few users. And this can be done in File systems too but it need high level knowledge on OS and other computer knowledge.
