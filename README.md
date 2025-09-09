# DAA-assignment

# Quick Sort Implementation in Python

## 📌 Overview
This project contains a simple **Quick Sort** implementation in Python.  
Quick Sort is a **divide-and-conquer** sorting algorithm that works by selecting a **pivot element**, partitioning the array into sub-arrays (elements less than, equal to, and greater than the pivot), and recursively sorting the sub-arrays.

---

## 📝 Code Explanation
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    
    pivot = arr[len(arr) // 2]   # Choose the middle element as pivot
    left = [x for x in arr if x < pivot]      # Elements less than pivot
    middle = [x for x in arr if x == pivot]   # Elements equal to pivot
    right = [x for x in arr if x > pivot]     # Elements greater than pivot
    
    return quick_sort(left) + middle + quick_sort(right)
