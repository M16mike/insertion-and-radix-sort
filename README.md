# insertion-and-radix-sort
the javascript code for implementing insertion and radix sort
Radix Sort is a unique, non-comparative sorting algorithm that sorts integers by processing individual digits. It separates numbers into individual digits and treats them as separate lists for sorting. Radix Sort stands out from other sorting algorithms as it does not perform comparison to sort values; instead, it utilizes the numeric value of each digit.

Radix Sort Function
The 'radixSort' function is the main function that implements the Radix Sort algorithm. It uses the helper functions 'getDigit', 'digitCount', and 'mostDigits' to sort an array of integers. It first identifies the maximum number of digits among the numbers using 'mostDigits', then sorts them digit by digit, from least significant to most significant, using digit buckets.
Insertion sort is one of the more intuitive sorting algorithms. Despite it being less efficient than algorithms such as Merge Sort and Quick Sort, it is able to outperform them in certain use cases.

Insertion Sort takes an array, puts it in order, and spits it out:

Insertion Sort an array
Insertion Sort is a stable, in-place, and comparison-type algorithm.

Stable means that two elements with equal values will appear in the same order in the sorted output as they appear in the unsorted input array.

For example, if we wanted to sort:

[“Cherries“, “Blackberries”, “Apples”, “Bananas”]

into alphabetical order by first letter, the output would be:

[“Apples”, “Blackberries”, “Bananas”, “Cherries”]

As you can see, “Blackberries” and “Bananas” remained in the same relative positions in the input and output array because the algorithm is stable. Bubble Sort, Merge Sort, and Radix Sort are also stable sorting algorithms.

If the algorithm was unstable, then “Bananas” and “Blackberries” may be interchanged. Selection Sort, Heap Sort and Quick Sort are examples of unstable sorting algorithms.

For a good and simple example of when it’s important to know whether an algorithm is stable or not, check out this article: Important Algorithm Concepts | Algorithm Stability, In-place Algorithms, and Comparison Algorithms

What’s an in-place algorithm? Here’s Wikipedia’s answer: “an algorithm which transforms input using no auxiliary data structure. However, a small amount of extra storage space is allowed for auxiliary variables.”

In simple terms, it usually just means that the input is overwritten (via swapping or replacement) by the output as the algorithm executes. The advantage of in-place algorithms is that they take up less space in memory.

And finally, a comparison sort is a sorting algorithm that only reads the list of elements through a single abstract comparison operation (usually a “less than” or “equal to”) that determines which of the two elements should occur first in the final sorted output array.

Insertion Sort step-by-step
Insertion Sort works by comparing an element with the elements to its left, until it reaches an element that is smaller than it; the element is then inserted in front of the smaller element.

Pass the unsorted array [5, 2, 4, 6, 1, 3] into Insertion Sort.
Start at the second element (2) of the array and compare it with its neighbouring element to the left (5).
Is 2 < 5? Yes, so insert 2 into 5’s place => [2, 5, 4, 6, 1, 3]
Now move up to the 3rd element (4) and compare with the value to the left (5).
Is 4 < 5? Yes, so move to the next element on the left.
Is 4 < 2? No, so insert in front of 2 => [2, 4, 5, 6, 1, 3]. As you can see, the numbers in bold are in order.
Now move up to the 4th element (6) and compare with the value to the left (5).
Is 6 < 5? No, leave where it is => [2, 4, 5, 6, 1, 3].
Now move up to the 5th element (1) and compare with the value to the left (6).
Is 1 < 6? Yes.
Is 1 < 5? Yes.
Is 1 < 4? Yes.
Is 1 < 2? Yes. We have reached the beginning of the array, so insert at front => [1, 2, 4, 5, 6, 3].
Now move up to 5th element (3) and compare with the value to the left (6).
Is 3 < 6? Yes.
Is 3 < 5? Yes.
Is 3 < 4? Yes.
Is 3 < 2? No => Insert after 2 => [1, 2, 3, 4, 5, 6]. The array is now sorted!
