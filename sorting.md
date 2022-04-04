# Sort Implementations & Big O Complexities

First of all, what is sorting? Sorting is when you are placing items in a list in order based on what you require. We use sorting algorithms to be efficient and sort everythiing that we need properly. 

## 1. Bubble Sort

Bubble sort is a sorting method which is fairly simple to go through. All you need to do is create a temporary variable that can take in the value from one of your main variables to make space for another variable. 

Here is an example picture of Bubblesort: 

```
for (int x = 0; x < array.size(); x++) {
            for (int y = 0; y < array.size() - 1; y++) {
                if (array.get(y) > array.get(y + 1)) {
                    int temporary = array.get(y);
                    array.set(y, array.get(y + 1));
                    array.set(y + 1, temporary);
                }
            }
        }
```

Basically all this code is doing is first getting our 2 variables: x and y. Each one has a certain value, but we want to switch, for example. To do this, we create a temporary variable, called "temporary" which will essentially just take the value of x and store until we can switch the value of y into x. Once we switch it, we take the value from the temporary variable and just input it in the y value. Boom! We have switched the variables

According to simplielearn, "This algorithm has a worst-case time complexity of O(n2). The bubble sort has a space complexity of O(1). The number of swaps in bubble sort equals the number of inversion pairs in the given array."

## 2. Selection Sort

Selection sort is another type of sorting method. The way it works is it constantly finds the lowest number in the list from the unsorted part and drops it at the beginning of the list. It  uses 2 subarrays to make sure that it sorts properly. It keeps iterating through the sorted codes until it doesn't have to do anything anymore. 

![image](https://user-images.githubusercontent.com/55414361/161598071-2a80264a-5a30-431f-acbe-23a57437c0ef.png)

Here is a flowchart of that process, from the geeksforgeeks website. 

It's a fairly simple process that just iterates through the code and constantly drops the lowest number to the front of the list until you don't anything. 

According to Wikipedia, "In computer science, selection sort is an in-place comparison sorting algorithm. It has an O(n2) time complexity, which makes it inefficient on large lists, and generally performs worse than the similar insertion sort."

## 3. Insertion Sort

Insertion sort is another type of sorting type. This is also a pretty simple algorithm. This also splits into subarrays with a sorted and unsorted part. 

Here is a code snippet that looks at this: 

```
public static void insertSort(ArrayList<Integer> array) {
        int n = array.size();
        for (int i = 1; i < n; ++i) {
            int key = array.get(i);
            int j = i - 1;
            while (j >= 0 && array.get(j) > key) {
                array.set(j + 1, array.get(j));
                j = j - 1;
            }
            array.set(j + 1, key);
        }

    }
```

In this code section, the code is essentially just iterating through the entire list and comparing the select number to it's predecessors. If the number before it is smaller, then it will stay in place. It keeps looking through it's ancestors until it finds a number that it is bigger than itself, and then it will switch into the spot before it. It does this process for each object in the code and will continue until it compeltely sorts itself. 

According to brilliant.org, "When analyzing algorithms, the average case often has the same complexity as the worst case. So insertion sort, on average, takes O ( n 2 ) O(n^2) O(n2) time. Insertion sort has a fast best-case running time and is a good sorting algorithm to use if the input list is already mostly sorted."

## 4. Merge Sort

Merge Sort is also another type of sorting method. To make the code more efficient, divides the array into two halves, sorts, and then merges those sorted code. 

Here is an example flow chart from Geeksforgeeks:

![image](https://user-images.githubusercontent.com/55414361/161598990-60455f81-53ad-42de-863a-5c2ddddedb45.png)

First it divides the array into two parts. Then it uses the sorting function for the first half and then continues onto the second one. Then it checks the two halves and then sorts them together using the merge sort. 

According to Medium.com, "Overall time complexity of Merge sort is O(nLogn). It is more efficient as it is in worst case also the runtime is O(nlogn) The space complexity of Merge sort is O(n). This means that this algorithm takes a lot of space and may slower down operations for the last data sets"
