# Intermediate java 03 MAR

## We did an exercise to merge to arrays. 
````
int[] arr1 = {3, 10, 15, 25, 30};
int[] arr2 = {4, 7, 11, 12};
int[] arr3 = new int[arr1.length+arr2.length];

int total = arr1.length+arr2.length;
int i = 0;
int j = 0;
int k = 0;

while (i <= arr1.length-1 && j <= arr2.length-1){
    if (arr1[i] < arr2[j]){
        arr3[k] = arr1[i];
        k++;
        i++;
    }
    else{
        arr3[k] = arr2[j];
        k++;
        j++;
    }
}

while (i <= arr1.length-1){
    arr3[k] = arr1[i];
    k++;
    i++;
}

while(j <= arr2.length-1){
    arr3[k] = arr2[j];
    k++;
    j++;
}

for (int q: arr3){
    System.out.print(q + " ");
}
````
## Recursion
- Any recursive solution can be solved iteratively.

**we did an the recursion.java problem. 

