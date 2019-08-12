##### Step by steps

- Using String split() method and assign substrings into array of strings.
- Create ArrayList and copy the element of string array to newly created ArrayList using Arrays.asList() method.

###### Program to convert String to ArrayList

```
public class JavaExample {
    public static void main(String args[]){
        String hello = "Hello world My name is truong dam";
        String str[] = hello.split(" ");
        List<String> arrStr = new ArrayList<String>();
        arrStr = Arrays.asList(str);

        for(String s: arrStr){
            System.out.println(s);
        }

    }
}
```

Output

```
Hello
world
My
name
is
truong
dam
```
