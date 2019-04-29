* Mutable object: Change the states and field after object is created
* Immutable object: Don't change anything after object is created

#### Example
* String is immutable object.
* StringBuffer, StringBuilder are mutable object. StringBuffer is synchronize and StringBuilder isn't

#### Java Mutable Example
Normally, it provides a method to modify the field value, and the object can be extended.
```
public class MutableClass {
    private String name;
    MutableClass(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    // this setter can modify the name
    public void setName(String name) {
        this.name = name;
    }

    public static void main(String[] args) {
        MutableClass obj = new MutableClass("hdtruong");
        System.out.println(obj.getName());

        // update the name, this object is mutable
        obj.setName("new hdtruong");
        System.out.println(obj.getName());

    }
}
```

#### Java Immutable Example
To create an Immutable object, make the class final, and don’t provide any methods to modify the fields.

```
public class ImmutableClass {
    private String name;
    ImmutableClass(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    // no setter

    public static void main(String[] args) {
        ImmutableClass obj = new ImmutableClass("hdtruong");
        System.out.println(obj.getName());

        // there is no way to update the name after the object is created.
        // And can't extend ImmutableClass
    }
}
```
Ref: [mkyong](https://www.mkyong.com/java/java-mutable-and-immutable-objects/)
Please refer to the Effective Java Book – Item 15: Minimize mutability.
