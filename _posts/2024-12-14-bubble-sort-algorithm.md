---
layout: post
title:  "Bubble Sort Algorithm"
date:   2024-12-14 23:49:12.519036644 +0000
categories: algorithms
---


The Bubble Sort is an algorithm that sorts the array from the lowest to the highest value. Learning it is quite useful when starting to learn about algorithms, even though there's not many use cases for it. 
My goal here is a full comprehension of the algorithm and be able to explain how this works and how I implemented that. 
It has a O(n²) complexity on average [Big-O Chart Complexity](https://www.bigocheatsheet.com/), but it is reaaaally fast when you have an Array that is nearly sorted. 

## So how it works? 
We loop through the array as many times as it has values inside it, so...
1. One value at a time;
2. If the current value is higher than the next value, we swap them. The highest values will come last;

![Bubble Sort](/images/bubble-sort-sequence-complete.png)

Here's possible to check that with the first passing through, the number 9 changed its place with the number 1, and all the other values stayed the same.
On the second loop, something like that will happen:
```
[3, 1, 9, 10, 23]
[1, 3, 9, 10, 23]
```
And we're done, our array is sorted. 

## Coding
You remember what I said before that the loop will go through as many times as it has values inside the array, so it is equivalent to the array size. But we also have a wise way of implementing the bubble sort in a way that, with nearly sorted arrays - like ours - the loop will stop as soon as no more items were sorted inside it. 

### Ruby Version:

```ruby
### basic version
array = [3, 9, 1, 10, 23]

looping = array.size - 1 # The index starts at 0, so we fix the size for that

looping.times do |current_loop|
  (looping - current_loop).times do |index| # Having nested loops makes it a O(n²)
    if(array[index] > array[index + 1])
      temp = array[index]                   # Create a temporary variable to hold the value.
      array[index] = array[index + 1]
      array[index + 1] = temp
    end
  end
end

### optimised version

array = [3, 9, 1, 10, 23]

looping = array.size - 1 # The index starts at 0, so we fix the size for that

looping.times do |current_loop|
  swapped = false
  
  (looping - current_loop).times do |index| # Having nested loops makes it a O(n²)
    if(array[index] > array[index + 1])
      temp = array[index]                   # Create a temporary variable to hold the value
      array[index] = array[index + 1]
      array[index + 1] = temp
      swapped = true
    end
  end

  break unless swapped # We stop the loop as soon as any changes have been made
end

p array

```

### Java version:

```java
import java.util.Arrays;

public class Main {

    public static void main(String[] args) {
        Integer[] array = {3, 9, 1, 10, 23};

        int size = array.length - 1;
        // Times that the loop will happen
        for (int i = 0; i < size; i++) {
            boolean swapped = false;

            // Compare and swap
            for (int j = 0; j < size  - i; j++) { //
                System.out.println(Arrays.toString(array));
                if(array[j] > array[j + 1]) {
                    int temp = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = temp;
                    swapped = true;
                }
            }

            if(!swapped) {
                break;
            }
        }

        System.out.println(Arrays.toString(array));
    }
}
```

Another useful resource about Sorting Algorithms is this [website](https://www.toptal.com/developers/sorting-algorithms) that "[...] illustrate how effectively data sets from different starting points can be sorted using different algorithms."

Feel free to add any suggestions and comments. 
Thank you 👋