# Java 8 with AspectJ Weaver Image

Sets `ASPECTJ_BINARY` to location of the jar file.

Example use case:
```
java -Xmx1400m -server -javaagent:$ASPECTJ_BINARY -Duser.timezone=UTC -jar /main.jar
```
