---
title: Implement Bubble Sort
---
# Implement Bubble Sort

---
## Problem Explanation
- Bubble Sort is a sorting algorithm which sorts or *bubbles* the largest number as last element at the end of each pass.
- We compare each element to the one ahead of it, if the element before is smaller, we swap their places.
- Bubble Sort's time complexity is **O(n<sup>2</sup>)**.
- It's a **stable** algorithm.
- ![Bubble sort in action](https://upload.wikimedia.org/wikipedia/commons/c/c8/Bubble-sort-example-300px.gif)


---
## Solutions

<details><summary>Solution 1 (Click to Show/Hide)</summary>

```js
function swap(a, b, arr) {
  let tmp = arr[a];
  arr[a] = arr[b];
  arr[b] = tmp;
}
function bubbleSort(array) {
  for (let i = 0; i < array.length; i++) {
    for (let j = 0; j < array.length - 1 - i; j++) {
      // -i because the largest element will be bubbled at the end so we don't have to compare.
      if (array[j] > array[j + 1]) {
        swap(j, j + 1, array);
      }
    }
  }
  return array;
}
```
</details>

<details><summary>Solution 2 (Click to Show/Hide)</summary>

```js
function bubbleSort(array) {
  for (let i = 0; i < array.length; i++) {
    for (let j = 0; j < array.length - 1 - i; j++) {
      if (array[j] > array[j + 1])
        [array[j], array[j + 1]] = [array[j + 1], array[j]]; // Using ES6 array destructuring to swap
    }
  }
  return array;
}
```
    
  #### Relevant Links
- [GeeksForGeeks](https://www.geeksforgeeks.org/bubble-sort/)
- [Wikipedia](https://en.wikipedia.org/wiki/Bubble_sort)
- Video by [HackerRank](https://www.youtube.com/watch?v=6Gv8vg0kcHc)
</details>
