

- **Memory Allocation in Java Variables/Classes/Functions**
- **JVM & JRE & JDK**
- **Cyclic Import**
- **Return Types of functions**

* Java Equals() vs hashCode()
   * https://www.geeksforgeeks.org/equals-hashcode-methods-java/
   * https://www.geeksforgeeks.org/override-equalsobject-hashcode-method/

* Iterator vs Enumeration
   * https://www.geeksforgeeks.org/difference-between-iterator-and-enumeration-in-java-with-examples/ 


* When to use Character Stream over Byte Stream? 
    * In Java, characters are stored using Unicode conventions. Character stream is useful when we want to process text files. These text files can be processed character by character. A character size is typically 16 bits.

* When to use Byte Stream over  Character Stream? 
    * Byte oriented reads byte by byte.  A byte stream is suitable for processing raw data like binary files.

* Names of character streams typically end with Reader/Writer and names of byte streams end with InputStream/OutputStream
* It is always recommended to close the stream if it is no longer in use. This ensures that the streams won't be affected if any error occurs.
