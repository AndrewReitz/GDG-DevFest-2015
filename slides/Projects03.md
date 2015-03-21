#### Projects

### Parcelable

```java
public final class Person implements Parcelable {
  private final int id
  private final String firstName
  private final String lastName

  public void writeToParcel(Parcel out, int flags) {
    out.writeInt(id);
    out.writeString(firstName);
    out.writeString(lastName);
  }

  public static final Parcelable.Creator<Person> CREATOR
    = new Parcelable.Creator<Person>() {
    public Person createFromParcel(Parcel in) {
      return new Person(in);
    }

    public Person[] newArray(int size) {
      return new Person[size];
    }
  };

  private Person(Parcel in) {
    id = in.readInt();
    firstName = in.readString();
    lastName = in.readString();
  }

  public getId() { return id; }
  public getFirstName { return firstName; }
  public getLastName { return lastName; }
}
```