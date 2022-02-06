# Notes from CS50x's Week 3 Lecuture: `Algorithms`
I am really excited for this week. Looks like we are gonna learn about the search algorithms.

- Algorithms are always related to runtime and that's why we need them as effiecient as possible.

### Big 'O' Notation
Used to represent the runtime of an algorithm.(or function in maths).(*how much it goes up in time*) Example representation:
```
O(n) | O(n/2) | O(log2 n)

```
'O' means `on the order of`.
**The less value between the notation, the more efficient the algorithm is.**
Common big 'O' notations:
- O(n²) [Worst one]
- O(n log n)
- O(n)
- O(log n)
- O(1) [The best one]
>Highest possible result for the algorithm

### Omega Notation(Ω)
The same as big 'O' but for how much it goes down in time.(*the bigger the more efficient**).
- Ω(n²)
- Ω(n log n)
- Ω(n)
- Ω(log n)
- Ω(1)
>The lowest possible result for the algorithm

---
## Linear Search
Going one by one(elements) linearly through the array(or so).

Then we can check with big O to determine the efficiency of this algorithm.
>Linear search upper bound score: O(n)[highest and worst case scenario]

>Linear search lower bound score: Ω(1)[lowest and best case scenario]

---
### Binary Search
(Like the phonebook contact search where we tear up the book in half and search in both halves.)
- If empty, stop.
- Numbers have to be sorted? 
- Then go to the middle and search there, 
- if it isn't the key, 
- if the current value is larger than the key, go to the left(smaller)half, else
- go to the right(larger) halfs
>Binary search upper bound score: O(log n)[I dont know why]

>Binary search lower bound score: Ω(1)

This search goes half by half: *64,32,16,8,4,2,1*

---
- numbers.c for implementing `Linear Search`
```C
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int numbers[] = {4,6,8,2,7,5,0};
    int key = get_int("Enter the key>|");
    for(int i=0;i < 7; i++)
    {
        if (numbers[i] == key)
        {
            printf("Found\n");
            printf("At index %i\n", i);
            return 0; //like quit
        }

    }
    printf("Not Found\n");
    return 1;
}
```
- names.c for implementing `` with strings
```C
#include <stdio.h>
#include <cs50.h>
#include <string.h>

int main(void)
{
    string names[] = {"Ken","John","Jack","Ben","Noopy"};
    string key = get_string("Enter key:|");

    for(int i = 0;i < 5;i++)
    {
        //strcmp compares strings by comparing every single ASCII character
        if (strcmp(names[i],key) == 0)
        {
            printf("Found at index %i\n",i);
            return 0;

        }
    }
    printf("404 Not Found!\n");
    return 1;

}
```
---
## Custom Data Types
Dictionaries and stuff?

>Ah yes. I remember this one from Siddhartha:

New data type declaration:
```C
typedef struct
{
    string name;
    string number;
}
person;
//new datatype person with those two values(strings )
```

Example program of searching inside the phonebook:
```C
#include <cs50.h>
#include <stdio.h>
#include <string.h>
typedef struct
{
    string name;
    string number;
}
person;
int main(void)
{
    person people[2];
    people[0].name = "Ken";
    people[0].number = "09090990993";

    people[1].name = "V";
    people[1].number = "+0084884889";

    for (int i=0;i < 2; i++)
    {
        if(strcmp(people[i].name, "V")== 0)
        {
            printf("Found %s\n",people[i].number);
            return 0;
        }
    }
    printf("Not Found\n");
    return 1;
}
```

---
### Selection Sort
Selecting numbers and compare them with each other or stuff like that?

>Pseudocode for the sorting mechanism

For i form 0 to n-1,
    - Find smallest item between i'th item and last item
    - Swap smallest item with i'th item

- `Big O Notation` = O(n²)
- `Omega Notation` = Ω(n)?

`Really not efficient algorithm`.
---
### Bubble Sort
Biggest number getting bubbled up to the rightmost side or larger side and smallest numbers to the left side.

>Pseudocode
- Repeat until sorted
  - For i from 0 to n-2
    - if i'th and i+1'th elements out of order
    - swap them
  - If no swaps
    - quit

`Big O Notation` : O(n²)

`Omega Notation`: Ω(n)
`Still the same with selection sort,in terms of the efficienty.`

---
## Recursion
Ability for a function to call itself. Very fragile and we can screw it up really easily. 
- No implementation. Looks like we're gonna have to do it in problem sets.
---
### Merge Sort
*Mind bending algorithm :)*

>Pseucode
1. If only one number(*on left half/right half*)
   1. Quit
2. Sort left half of numbers
3. Sort right half of numbers
4. Merge sorted halves
5. Compare and compare the left sided numbers and right sided numbers one by one.(As Brain visualized.)

- Have to do `n` things `log n` times.
- Needs an extra array to put the sorted numbers into.
- Speed Efficient but not space/memory efficient.

`Big O Notation: O(n log n)`

`Omgea Notation: Ω(n log n)`


### Theta Notation(Θ)
When the upper bound(`Big O Notation`) and the lower bound(`Omega Notation`) of an algorithm are the same. We can just describe it with the `Theta Notation(Θ)`.

`Selection sort: Θ(n²)`

`Merge sort: Θ(n log n)`


And Done with the video. 

----
# Shorts

### Linear Search
### Binary Search
- *the array had to be sorted*
- Get the middle. If key > middle, only search in the right side. If key < middle, the left side.

### Bubble Sort
- Smallest to the left side, largest to the right side everytime.

### Selection Sort
- Add smallest value to the end of the sorted list.(first smallest one will go to the first place.)
### Recursion
