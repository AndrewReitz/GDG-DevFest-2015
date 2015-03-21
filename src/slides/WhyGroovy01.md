### Why Groovy

Java Model

```java
public final class Person {
  private final String firstName;
  private final String lastName;
  public Person(String firstName, String lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
  }
  public String getFirstName() { return firstName; }
  public String getLastName() { return lastName; }
  @Override public boolean equals(Object o) { /*lots of code here*/ }
  @Override public int hashCode() { /*lots of code here*/ }
  @Override public String toString() { /*lots of code here*/ }
}
```
