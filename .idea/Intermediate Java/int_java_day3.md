# Intermediate Java Day 3

### Transferred code for note taking into packages inside the java file project intermediate_java

## Arrays Continued 
- We spent the first third of class working through the previous exercise where we created an array to manage adding students to a class.

## Searching and Sorting
- Did an activity where we searched for a specific value in an array. This was my solution. 


    for (int i = 0; i < theArray.length; i++) {
        if (theArray[i] == userInput) {
            System.out.println("The number " + userInput + " exists in the array at index " + i);
        } 
    }


- Another way to acoomplish it using a a FOR EACH loop, while it is less complicated it does not give us the index of the value.


    for (int x : theArray) {
        if (x == userInput) {
            System.out.println("The number " + userInput + " exists in the array at index " + x);
            return;
        }
    }
    System.out.println("The number " + userInput + " does not exist in the array.");


## Array of Arrays


    int[][] theArray = {{1,2}, {3,4};

- this is an array of arrays. with the values arranged like this. 
- 1, 2 = first array
- 3, 4 = second array

### Exercise to print this. Correct answer is below:
    int[][] x {{1,2,3}, {4,5,6}};
    for (int i = 0; i < x.length; i++) {
    for (int j = 0; j < x[i].length; j++) {
    System.out.print(x[i][j] + " ");
    }
    System.out.println();
    }

### Next exercise was to get an array of arrays. Find the lowest number in each row and then input that number into a new one dimensional array of minimum numbers.

    int[][] x = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    int[] min = new int[x.length];
    for (int i = 0; i < x.length; i++){
        min[i] = x[i][0];
        for (int j = 1; j < x[i].length; j++){
            if (x[i][j] < min[i]){
                min[i] = x[i][j];
            }
        }
    }
    for (int i = 0; i < min.length; i++){
        System.out.print(min[i] + " ");
    }
}

- Note at the start of the for loop I compare the first value in the array with the first value in the min array. then offset that in the nested for loop. 

## Sorted and unsorted arrays. 
- remember big O notation and how we can use it to compare the time complexity of an algorithm.
- if we receive an unsorted array, it is more time efficient to sort it before searching for a value.