# Intermediate Java - Day 15

## Resilient Code
- When we work in industry it is important to create code that is resilient to errors.

## Exception Handling
- we use the Try and Catch block to handle errors
- we use the Throw keyword to throw an exception
- Finally block is always executed. Used for closing resources, open files or network connections.
- 
````
    public static void main(String[] args) {
        try{
            int[] x = {1,2,3,};
            System.out.println(x[4]);
        }
        catch(Exception e){
            System.out.println("Error");
            System.out.println(e);
        } finally{
            System.out.println("Finally");
        }
        System.out.println("End");
    }

````

**Will throw an object of type Exception**

````
        try{
            throw new IndexOutOfBoundsException("Just for Fun");
        }
        catch(IndexOutOfBoundsException e){
            System.out.println(e.getMessage());
        }
````

**This is an example of catching the exception and displaying a specified message**

```
        try{
            int x = 3;
            int y = 0;
            int[] a = {1,2,3};
            System.out.println(a[4]);
            int z = x / y;
            System.out.println(z);
        }
        catch (ArithmeticException e){
            System.out.println("Dude, Division by zero is not allowed");
        }
        catch(ArrayIndexOutOfBoundsException e){
            System.out.println("Dude, out of bounds!");

        } catch(Exception e){
            System.out.println("Exception");
        }
```

**If you want to do specific exceptions remember to use the children instances first**

## Two types of exceptions
- Checked exceptions
  - We have to handle and declared within the code
- Unchecked exceptions
  - We as a developer should be aware of these exception, although we do not necessarily need to handle them.

````
        //This works (unchecked)
        throw new ArithmeticException("Just for fun");
        
        //This does not work because it is a checked
        throw new IOException("Just for fun");
````

- We can also do a try in the parent block. For example.
  - The function does not catch the error but does the parent or calling method does.

```java
        try{
            func1();
        } catch (Exception e){
            System.out.println("Catch it here");
        }
    }
    public static void func1(){

            int x = 3;
            int y = 0;
            int z = x / y;
    }
```


