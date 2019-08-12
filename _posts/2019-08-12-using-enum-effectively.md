##### This is how to define Enum

```
public enum Animals {
    DOG,
    CAT
}
```

##### How to assign value to enum type?
```
Animals animal = Animals.CAT;
```

##### How to iterate through an Enum variable

```
for (Animals ani : Animals.values()){
    System.out.println(ani);
}
```

##### Enum Fieds and Methods

```
public enum Animals {
    DOG (1),
    CAT (2);

    private final int shortCode;

    Animals (int code){
        this.shortCode = code;
    }

    public int getAnimalCode(){
        return this.shortCode;
    }
}

public class EnumAnimals
{
    public static void main(String[] args) {
    	Animals ani = Animals.DOG;
    	System.out.println(ani.getAnimalCode());

    	Directions ani2 = Animals.CAT;
    	System.out.println(ani2.getAnimalCode());
    }
}
```

Output

```
1
2
```

As you can see in this example we have a field shortCode for each of the constant, along with a method getAnimalCode() which is basically a getter method for this field. When we define a constant like this DOG (1), it calls the enum constructor (Refer the constructor Directions in the above example) with the passed argument. This way the passed value is set as an value for the field of the corresponding enum’s constant [DOG(1) => Would call constructor Animals(1) => this.shortCode = code => this.shortCode = 1 => shortCode field of constant DOG is set to 1].
