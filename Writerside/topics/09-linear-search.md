# Linear Search in Java

In the realm of computer science and programming, searching is a fundamental operation. It involves finding a specific
element within a collection of elements. One simple yet essential searching algorithm is the **Linear Search**.

## What is Searching?

Searching is the process of finding a particular item in a collection of items. It is a common operation in many
applications, ranging from databases to everyday programming tasks.

## Linear Search

Linear Search is a straightforward searching algorithm that traverses a list sequentially to find a target element. It
iterates through each element until a match is found or the entire list is searched. While not the most efficient
algorithm for large datasets, it is easy to implement and applicable in various scenarios.

<img src="https://miro.medium.com/v2/resize:fit:960/1*JKAotHLxIfO9GH5iQRnH4A.jpeg" alt="linear search image" border-effect="rounded"/>

## Linear Search Algorithm

1. Start at the beginning of the list.
2. Compare the target element with the current element.
3. If a match is found, return the index of the current element.
4. If the end of the list is reached without finding a match, return -1 to indicate that the element is not present.

## Pseudocode

```
function linearSearch(array, target):
    for each element in array:
        if element equals target:
            return index of element
    return -1 // Element not found
```

## Code for Linear Search

Let's delve into a basic implementation of Linear Search in Java:

```java
public class LinearSearch {
    public static int linearSearch(int[] arr, int target) {
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == target) {
                return i; // Element found, return its index
            }
        }
        return -1; // Element not found
    }

    public static void main(String[] args) {
        int[] array = {5, 12, 7, 3, 9, 20};
        int targetElement = 7;
        int result = linearSearch(array, targetElement);

        if (result != -1) {
            System.out.println("Element found at index: " + result);
        } else {
            System.out.println("Element not found in the array.");
        }
    }
}
```

## Time Complexity

The time complexity of the Linear Search algorithm is O(n), where 'n' is the number of elements in the list or array. It
performs a constant amount of work for each element in the worst case.

## 🎯 Questions

### Q1: Search in String

Write a Java function to perform a linear search for a specific character in a given string.

```Java
package A06_searching.src;

import java.util.Objects;
import java.util.Scanner;

public class Linear_search_strings {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        System.out.println("Enter the element you want to find: ");
        String[] array = {"ranit", "manik", "is", "god"};
        String target = in.nextLine();
        // calling the function ==>
        System.out.println("The index of the searching element is: " +
         linear_search(array, target)); // index starts from '0' in the java
    }

    // searching in the array: return the index if found the item
    // otherwise if item not found return '-1'
    static int linear_search(String[] arr, String target) {
        if (arr.length == 0) {
            return -1;
        }

        // run a for loop ==>
        for (int index = 0; index < arr.length; index++) {
            // check for an element at every index if or is == target ==>
            String element = arr[index];
            if (Objects.equals(element, target)) {
                return index;
            }
        }
        // this line will execute ==> 
        // if none of the above return statements have executed
        // ==> no return statement has been hit in the function
        // ==> hence the target is not found
        return -1; // as '-1' cannot be an index value
    }
}
```

### Q2: Search in Range

Modify the linear search code to search for an element within a specified range in an array.

```Java
package A06_searching.src;

public class search_in_range {
    public static void main(String[] args) {
        int[] nums = {23, 56, 45, 89, 74, 75, 95, 42, 26, 84, 31, 13};
        int target = 89;
        // calling the function ==>
        System.out.println("The index of the searching element is: " + 
        linear_search(nums, target, 0, 5)); 
        // index starts from '0' in the java
    }

    // searching in the array: return the index if found the item
    // otherwise if item not found return '-1'
    static int linear_search(int[] arr, int target, int start, int end) {
        if (arr.length == 0) {
            return -1;
        }

        // run a for loop ==>
        for (int index = start; index <= end; index++) {
            // check for an element at every index if or is == target ==>
            int element = arr[index];
            if (element == target) {
                return index;
            }
        }
        // this line will execute ==>
        // if none of the above return statements have executed
        // ==> no return statement has been hit in the function
        // ==> hence the target is not found
        return -1;
    }
}
```

### Q3: Minimum Number

Implement a linear search to find the minimum number in an array.

```Java
package A06_searching.src;

import java.util.Arrays;

public class Find_minimum_number {
    public static void main(String[] args) {
        int[] arr = {12, 51, 65, 654, 32, 547, 98, 15};
        System.out.println(Arrays.toString(arr));
        System.out.print("The minimum number is: " + min(arr));
    }

    // assume arr.length != 0 ==>
    // return the minimum value in the array ==>
    static int min(int[] arr) {
        int min = arr[0]; 
        // assuming the first element is the minimum number
        for (int j : arr) { 
        // enhanced for loop which will 'min' the element if any element < min
            if (j < min) {
                min = j;
            }
        }
        return min;
    }
}

```

### Q4: Search in 2D Arrays

Extend the linear search algorithm to work with a two-dimensional array.

```Java
package A06_searching.src;

import java.util.Arrays;
import java.util.Scanner;

public class Search_in_2D_array {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        // declaring and printing the array ==>
        int[][] arr = {
                {23, 341, 65},
                {26, 31},
                {45, 41, 55, 56},
                {18, 22}
        };
        for (int[] ints : arr) {
            System.out.println(Arrays.toString(ints));
        }

        // taking input of the searching element ==>
        System.out.print("Enter the element you want to search: ");
        int target = in.nextInt();

        // printing the array with row and col no of search element ==>
        System.out.print("The following array contains 
        row and column of the searching element: ");
        
        System.out.println(Arrays.toString(search(arr, target)));
        // format of return value (array) ==> {row, col}
    }

    static int[] search(int[][] array, int target) {
        for (int row = 0; row < array.length; row++) {
            for (int col = 0; col < array[row].length; col++) {
                if (array[row][col] == target) {
                    return new int[]{row, col}; 
                    // creating and returning a new array which contains ==> 
                    // {row, col} elements
                }
            }
        }
        /*
        this is enhanced for loop you can go with ==>
        for (int[] ints : array) {
            for (int anInt : ints) {
                if (anInt == target) {
                    return 1;
                }
            }
        }
         */
        return new int[]{-1, -1};
    }
}
```

### Q5: Even Digits

Question link: <https://leetcode.com/problems/find-numbers-with-even-number-of-digits/>

```Java

package A06_searching.src;
public class EvenDigits {
    public static void main(String[] args) {
        int[] nums = {12,345,2,6,7896};
//        System.out.println(findNumbers(nums));

        System.out.println(digits2(-345678));
    }
    static int findNumbers(int[] nums) {
        int count = 0;
        for(int num : nums) {
            if (even(num)) {
                count++;
            }
        }
        return count;
    }

    // function to check whether a number contains even digits or not
    static boolean even(int num) {
        int numberOfDigits = digits(num);
        /*
        if (numberOfDigits % 2 == 0) {
            return true;
        }
        return false;
         */
        return numberOfDigits % 2 == 0;
    }

    static int digits2(int num) {
        if (num < 0) {
            num = num * -1;
        }
        return (int)(Math.log10(num)) + 1;
    }

    // count number of digits in a number
    static int digits(int num) {

        if (num < 0) {
            num = num * -1;
        }

        if (num == 0) {
            return 1;
        }

        int count = 0;
        while (num > 0) {
            count++;
            num = num / 10; // num /= 10
        }

        return count;
    }
}
```

### Q6: Max Wealth

Question link: <https://leetcode.com/problems/richest-customer-wealth/>

```Java
package A06_searching.src;
public class MaxWealth {
    public static void main(String[] args) {

    }
    public int maximumWealth(int[][] accounts) {
        // person = rol
        // account = col
        int ans = Integer.MIN_VALUE;
        for (int[] ints : accounts) {
            // when you start a new row, take a new sum for that row
            int sum = 0;
            for (int anInt : ints) {
                sum += anInt;
            }
            // now we have sum of accounts of person
            // check with overall ans
            if (sum > ans) {
                ans = sum;
            }
        }
        return ans;
    }
}
```

Feel free to explore and experiment with these questions to deepen your understanding of linear search in Java. Happy
coding!