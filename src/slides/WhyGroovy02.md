### Why Groovy

Groovy Model

```groovy
@Immutable
final class Person {
  private final String firstName
  private final String lastName
}

def person1 = new Person("Leslie", "Knope")
def person2 = new Person(firstName: "Ben", lastName: "Wyatt") // Named constructors!
```

Note:
Groovy constructors are pretty sweet!
