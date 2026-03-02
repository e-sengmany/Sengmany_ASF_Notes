# Intermediate Java - Day 5

### First part of class we were given the exercise to write a program that will have a class student wit attributes: name, GPA. We then took user input and stored instances of the class student into a studdent array.

### ArrayLists
- ArrayLists are used to store objects.
- have the following methods:
  - add()
  - remove()
  - get()
  - set()
- ArrayList<String> list_name = new ArrayList<String>();
  - Array list is a class. 

### ** Cannot create an array list of a primitive type.**
- We made an array list of students and then sorted them. 

````
    public class Student implements Comparable<Student>
````
- We can extend the class student and implement the compareTo method.
````
    public int compareTo(Student s){
        return this.age - s.age;
    }
````
- Tells the program what exactly to compare

````
   Collections.sort(students);
````
- Sorts the array list by comparing the ages