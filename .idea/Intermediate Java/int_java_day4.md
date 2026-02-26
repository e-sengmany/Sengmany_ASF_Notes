# Day 4

### We started the class by using binary search.
- We took the program from last class and use the below code to search it for a a specific number.
- We halved the code to search that half for the number to speed up the search process.

`

    while (l <= h){
    //establishes the midpoint
    m = (l + h)/2;
    //if the number is the midpoint initially it will be complete otherwise
    if(m == search){
        System.out.println("found");
        return;
    }
    //midpoint is smaller that the search then we raise the lower limit
    else if(m < search){
        l = m + 1;
    }
    //midpoint is larger than the search then we lower the upper limit
    else{
        h = m - 1;
    }
    }

`

We then moved to an exercise that takes a number and checks to see if it is a palindrome (same values on both sides, ex: 1331)

`

    int d = 1331;
    //example of changing it to a string.
    String s = String.valueOf(d);
    int l = 0;
    System.out.println(s.length());
    int h = s.length() - 1;
    System.out.println(h);
    while (l < h){
    System.out.println(s.charAt(l) + " " + s.charAt(h));
    if(s.charAt(l) != s.charAt(h)){
    System.out.println("not a palindrome");
    return;
    }
    l++;
    h--;
    }
    System.out.println(d + " is a palindrome");

`

- Now we want to do it using the modulus operator.

````
    int original = 1331;
    int newone = 0;
    int value = original;
    while(value > 0)
    {
        int digit = value%10; //1331%10 == 1
        value = value/10;     //1331/10 = 133
        newone = newone*10 + digit; //133*10 + 1 = 1331
        //this is essesntially extracting the last digit and rebuilt the number from the end to the beginning. If it matches then it is a palindrome.  
    }
    if(original == newone)
    {
        System.out.println(original + " is a palindrome");
    }
    else
    {
        System.out.println(original + " is not a palindrome");
    }
    
````