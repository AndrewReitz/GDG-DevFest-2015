### Why Groovy

Java File Read

```java
int len;
char[] chr = new char[4096];
final StringBuffer buffer = new StringBuffer();
final FileReader reader = new FileReader(new File("/path/to/file"));
try {
  while ((len = reader.read(chr)) > 0) {
      buffer.append(chr, 0, len);
  }
} finally {
  reader.close();
}
System.out.println(buffer.toString());
```

Note:
Have to look it up every time.
Commons-IO helps, but not enough
Missing try catch around close (auto close in java 7 but not supported in Android)
