# 04 MAR

### We started class doing two exercises. One was to count the sum on numbers ending at number n. The other was to print the numbers from 0 to n. 
````
public static void main(String[] args) {
    //int num = 12345;
    //System.out.println(addDigits(num));
    //int count = 8;
    //printNumbers(count);
    //printReverse(count);

    int[] arry = {3, 7, 2, 9, 8, 1, 5, 4};
    
}
public static int addDigits(int n){
    int num = n;
    if (num == 0){
        return 0;
    }
    else{
        return num%10 + addDigits(num/10);
    }
}
//write a program that will accep the number n and then it will print from 0 to n recursively
public static void printNumbers(int n){
    if (n == 0){
        System.out.println(0);
    }
    else{
        printNumbers(n-1);
        System.out.println(n);
    }
}
public static void printReverse(int n){
    if (n == 0){
        System.out.println(n);
        return;
    }
    else{

        System.out.println(n);
        printReverse(n-1);
    }

}
````

## Recursion, Merge Sort
- Recursion is a method that calls itself.
- Merge Sort is a sorting algorithm that uses recursion.
- We utilized the merge function for two arrays we wrote yesterday.

````
    public static void main(String[] args) {
        int[] arry = {3, 7, 2, 9, 8, 1, 5, 4};
        for(int q: arry){
            System.out.print(q + " ");
        }
        System.out.println();
        //we call mergeSort on the array, because the actual sorting is done with mergeTwoSortedArray that is done inside mergeSort
        int[] merged = mergeSort(arry, 0, arry.length-1);

        for (int q: merged){
            System.out.print(q + " ");
        }
    }
    
    public static int[] mergeTwoSortedArray(int[] arr1, int[] arr2){
        int[] arr3 = new int[arr1.length+arr2.length];
        //get a new total length of the two arrays.
        int i = 0;
        int j = 0;
        int k = 0;
    // Below is the merging and sorting of two arrays we did in the previous class.
        while (i <= arr1.length-1 && j <= arr2.length-1){
            //while loops is a requirement that will go until one of the arrays is empty.

            if (arr1[i] < arr2[j]){
                // if left array value is smaller than right, then that is the value placed into third array.
                arr3[k] = arr1[i];
                k++;
                i++;
            }
            else{
                //otherwise the right array value is placed into the third array.
                arr3[k] = arr2[j];
                k++;
                j++;
            }
        }

        while (i <= arr1.length-1){
            // Means that all the values in the left array have been placed into the third array.
            arr3[k] = arr1[i];
            k++;
            i++;
        }
            //Means that all the values in the right array have been placed into the third array.
        while(j <= arr2.length-1){
            arr3[k] = arr2[j];
            k++;
            j++;
        }

        return arr3;
    }

    public static int[] mergeSort(int[] arry, int start, int end){
        //We are going to use the divide and conquer method to sort the array.
        if (start >= end){ // while th left doesnt bleed into the right
            int[] temp = new int[1];
            temp[0] = arry[start];
            return temp;
        }
        // we make a mid point
        int mid = (start + end)/2;
        //we recursively call mergeSort on the left THEN the right
        int[] left = mergeSort(arry, start, mid);
        int[] right = mergeSort(arry, mid+1, end);

        //Then we merge them together
        int[] merged = mergeTwoSortedArray(left, right);
        return merged;

    }
````
- This function works by continually dividing the given array into two halves.
- Then we recursively call mergeSort on the left and right halves. Until the left and right halves are only 1 value.
- Then we merge the two halves together using mergeTwoSortedArray.