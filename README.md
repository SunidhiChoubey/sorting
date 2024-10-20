# Experiment-20
# sorting
## Aim- To study and implement Sorting Algorithm.
## Theory-
Sorting is a fundamental operation in computer science for organizing data. It can be done in ascending or descending order, and various sorting algorithms exist, including Selection Sort, Insertion Sort, and Bubble Sort. Here’s a summary of each:

1. Selection Sort:
Selection Sort repeatedly finds the smallest element from the unsorted part of the array and swaps it with the first unsorted element. This process continues until the array is sorted.

Steps:

Find the smallest element in the unsorted portion.
Swap it with the first element of the unsorted portion.
Move the boundary between sorted and unsorted elements.
Repeat until the entire array is sorted.
Example: For the array [29, 10, 14, 37, 14], after several passes, it becomes [10, 14, 14, 29, 37].

Time Complexity: O(n²) in all cases.

2. Insertion Sort:
Insertion Sort sorts the array by taking elements from the unsorted portion and inserting them into their correct positions in the sorted part.

Steps:

Assume the first element is sorted.
Take the next element, compare it with sorted elements, and shift them to make space.
Insert the current element into its correct position.
Repeat for all elements.
Example: For the array [12, 11, 13, 5, 6], it becomes [5, 6, 11, 12, 13] after sorting.

Time Complexity: O(n) in the best case, O(n²) in the worst case.

3. Bubble Sort:
Bubble Sort repeatedly compares and swaps adjacent elements if they are in the wrong order. The largest unsorted element "bubbles up" to its correct position at the end.

Steps:

Compare adjacent elements and swap if necessary.
Repeat the process, ignoring the sorted elements at the end.
If no swaps are made in a pass, the array is sorted.
Example: For the array [64, 34, 25, 12, 22, 11, 90], it becomes [11, 12, 22, 25, 34, 64, 90].

Time Complexity: O(n²) in the average and worst cases.
## Code-

~~~
#include <iostream>
using namespace std;

void swap(int *a, int *b) 
{
  int temp = *a;
  *a = *b;
  *b = temp;
}


void display(int ar[], int len) 
{
  for (int i = 0; i < len; i++) 
  {
    cout << ar[i] << " ";
  }
  cout << endl;
}

void selectsort(int ar[], int len) 
{
  for (int j = 0; j < len - 1; j++) 
  {
    int mi = j;
    for (int i = j + 1; i < len; i++) 
    {
      if (ar[i] < ar[mi])
        mi = i;
    }

    swap(&ar[mi], &ar[j]);
  }
}

int main() 
{
  int data[] = {50, 25, 10, 15, 30};
  int len = sizeof(data) / sizeof(data[0]);
  cout << "Original Array:";
  display(data, len);
  selectsort(data, len);
  cout << "Selection sorted array:";
  display(data, len);
}
~~~
b.
~~~
#include <iostream>
using namespace std;

void insertsort(int ar[], int n) 
{
    for (int i = 1; i < n; i++) 
    {
        int key = ar[i];
        int j = i - 1;

        while (j >= 0 && ar[j] > key) 
        {
            ar[j + 1] = ar[j];
            j = j - 1;
        }
        ar[j + 1] = key;
    }
}

void display(int ar[], int n) 
{
    for (int i = 0; i < n; i++) 
    {
        cout << ar[i] << " ";
    }
    cout << endl;
}

int main() {
    int ar[] = {12, 16, 2, 8, 6};
    int n = sizeof(ar) / sizeof(ar[0]);

    cout << "Original array: ";
    display(ar, n);
    insertsort(ar, n);
    cout << "Insertion Sorted array: ";
    display(ar, n);

    return 0;
}
~~~
c.
~~~
#include <iostream>
using namespace std;

void bubbleSort(int ar[], int len) 
{

  for (int j = 0; j < len -1; ++j) 
  {
      
    for (int i = 0; i < len - j - 1; ++i) 
    {

      if (ar[i] > ar[i + 1]) 
      {
        int temp = ar[i];
        ar[i] = ar[i + 1];
        ar[i + 1] = temp;
      }
    }
  }
}

void display(int ar[], int len) 
{
  for (int i = 0; i < len; ++i) 
  {
    cout << "  " << ar[i];
  }
  cout << "\n";
}

int main() 
{
  int data[] = {-11, 3, 0, 11, -1};
  int len = sizeof(data) / sizeof(data[0]);
  cout << "Original array: ";
  display(data, len);
  bubbleSort(data, len);
  cout << "Bubble Sorted array: ";  
  display(data, len);
}
~~~
## Output-
![](https://github.com/SunidhiChoubey/sorting/blob/main/Screenshot%202024-10-21%20024704.png)
1[](https://github.com/SunidhiChoubey/sorting/blob/main/Screenshot%202024-10-21%20024739.png)
![](https://github.com/SunidhiChoubey/sorting/blob/main/Screenshot%202024-10-21%20024819.png)
![](https://github.com/SunidhiChoubey/sorting/blob/main/Screenshot%202024-10-21%20024739.png)
## Conclusion-
We learnt about sorting in C++ and  We learnt the use case of the types of sorting in C++.




