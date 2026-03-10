# Intermediate Java Day 9

## Exam 1 review
- Sorting method he was describing during the exam is also known as quickSort.

````
public class Main {
    public static void main(String[] args) {
        int[] arr = {10, 8, 4, 12, 3, 17, 9, 8};

        qsort(arr, 0, arr.length-1);

        for(int i: arr){
            System.out.print(i + " ");
        }


    }

    public static void qsort(int[] arr, int low, int high){
        if(low <= high){ //base case that stops it because that means it overlaps.
            return;
        }

        int partition = partition(arr,low, high); // pick a number
        qsort(arr, low, partition-1); //low to the partition
        qsort(arr, partition+1, high);// partition to high
    }

    public static int partition(int[] arr, int low, int high){
        int pivot = arr[high]; //pick a number, people usually pick highest index
        int[] left = new int[high - low]; //left of the partition. So high minus low would be half
        int[] right = new int[high - low];// right of the partition

        int n1 = 0; //essentially how many items are in the left array
        int n2 = 0;// how many items are in the right array

        //test the array. anything lower than pivot will go into the left and anything higher will go to the right.
        for( int i = low; i<high-low-1;i++)
            if(arr[low+i] < pivot)
                left[n1++] = arr[low+i];
            else
                right[n2++] = arr[low+i];

        //We are now going to put the array back together based on order. So starting with left side.
        for(int i = 0; i<n1;i++) //go though the left array.
            arr[low+i] = left[i]; // so starting from the low point +1 we are adding the left array to the original array

        //Now we filled all left side, we put pivot back into the middle.
        arr[low + n1] = pivot; //put the pivot in the middle. So lowest plus the length of left array (which will be n1)

        //Now we fill in the right side with the remaining.
        for(int i = 0; i<n2;i++)
            arr[low+i+n1+1] = right[i]; //left limit pull partition would bring us to the middle, plus 1 to be on the right side of the pivot and i to iterate.

        return low+n1; // establishes new pivot. so we are halving the new one. so for the qsort on the left side we did one iteration to half and now we are going using this to half the current side.
    }
}

````

## Inheritance
- Classes can inherit from other classe, which allows them to share methods and variables.
- protected is a modifier that allows a class to access a variable or method that is in a parent class.
- private is a modifier that allows a class to access a variable or method that is in the same class.
- public is a modifier that allows a class to access a variable or method that is in any class.
- final, if you use this modifier, no class can inherit from it.

### Different types
- single inheritance
- multiple inheritance
- hierarchical inheritance
- multilevel inheritance
- hybrid inheritance

** When you instantiate a child, it will inherit all the variables and methods of the parent.

### Advantages vs Disadvantages
- Advantages:
    - Less code/more reusable
    - Modular and organized
    - Polymorphism support
- Disadvantages:
    - Tight coupling (rely on parent/child)
    - More bugs and complexity
    - Difficuly encapsulating