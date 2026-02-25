# Intermediate Java Day 2

## Arrays
-initialization of arrays is as follows:

string[] names = new string[5];
- 5 is the size of the array
- String is the type of data in the array

**once we define the length we cannot change it**


//int[] x = {3, 10, 20};

//was practice setting up an =array

int[] x = new int[4];

Scanner obj = new Scanner(System.in);

        for(int i=0; i < x.length; i++) {
            System.out.println("Enter a number: ");
            x[i] = obj.nextInt();
        }


### We used arrays to complete the program we attempted yesterday
-We noticed that we were able to actually able to store the employee names in the array and call them by referencing the index. 
````
    String[] employee = new String[5];
        int[] empAge = new int[5];
        int employeeCount = 0;

        boolean cont = false;

        while(!cont ){
            displayMenu();
            System.out.println("Enter choice");
            Scanner input = new Scanner(System.in);
            int choice = input.nextInt();
            switch(choice){

                case 1:
                    System.out.println("Employee Add");
                    if (employeeCount >= 5) {
                        System.out.println("Employee list is full");
                        break;

                    }
                    else if (employee[employeeCount] == null) {
                        System.out.println("Enter employee name:");
                        String employeeName = input.next();
                        if (employeeName.isEmpty() || employeeName == " ") {
                            System.out.println("Name cannot be empty");
                            employeeName = input.next();
                        }
                        input.nextLine();
                        System.out.println("Enter employee age:");
                        int employeeAge = input.nextInt();
                        if (employeeAge < 0) {
                            System.out.println("Age cannot be negative");
                            employeeAge = input.nextInt();
                        }
                        employee[employeeCount] = employeeName;
                        empAge[employeeCount] = employeeAge;
                        employeeCount++;
                        break;
                    }
                case 2:
                    System.out.println("You have selected Employee Average Age");
                    System.out.println("Average Age is: " + averageAge(empAge, employeeCount));
                    break;
                case 3:
                    System.out.println("Employee over certain age");
                    System.out.println("What age?");
                    int age = input.nextInt();
                    System.out.println("Number of employees over age " + age + " is: " + overAge(empAge, age));
                    break;
                case 4:
                    System.out.println("you have selected quit");
                    cont = true;
                    break;
                default: System.out.println("invalid choice");
            }
        }


    }
    public static void displayMenu(){
        System.out.println("please select an item from the menu:");
        System.out.println("    1. Add Employee");
        System.out.println("    2. Employee Average Age");
        System.out.println("    3. Employee over certain age");
        System.out.println("    4. Quit");

    }
    public static double averageAge(int[] empAge, int employeecount){
        double sum = 0;
        for(int i = 0; i < empAge.length; i++){
            sum += empAge[i];
        }
        return sum/employeecount;
    }
    public static int overAge(int[] empAge, int age){
        int count = 0;
        for(int i = 0; i < empAge.length; i++){
            if(empAge[i] > age){
                count++;
            }
        }
        return count;
    }
````
This was my solution for the problem.

## FOR EACH AKA Enhanced FOR LOOP
- for each is used to iterate through an array.
- it is used in conjunction with the enhanced for loop.
- it is used to iterate through an array and perform an action on each element.

    for (int x: age){
    System.out.println(x);
    }

where int x is the variable name and age is the array name.

````
    String[] names = {"John", "Eric", "Clint", "Alexander"};
    String[0] = "Bob";
````

- this is an example of how to change the value of an element in an array.

**Note: Arrays names are references**
- we cannot change the value of an array name.