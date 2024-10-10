```python
three_dimensional[::2,:, -1]
```

Let's break down the slicing `three_dimensional[::2, :, -1]`.

Given the array:

```python
array([[[ 0,  1,  2,  3,  4],
        [ 5,  6,  7,  8,  9]],

       [[10, 11, 12, 13, 14],
        [15, 16, 17, 18, 19]],

       [[20, 21, 22, 23, 24],
        [25, 26, 27, 28, 29]]])
```

### Slicing `three_dimensional[::2, :, -1]`

1. **First part `[::2]`:**
   - This means "take every 2nd element along the first axis (or 0th dimension), starting from the first one."
   - It selects the 1st and 3rd blocks (index 0 and index 2), skipping the 2nd block (index 1).
   - Specifically, it extracts:
     ```python
     [[[ 0,  1,  2,  3,  4],
       [ 5,  6,  7,  8,  9]],

      [[20, 21, 22, 23, 24],
       [25, 26, 27, 28, 29]]]
     ```

2. **Second part `[:, :]`:**
   - The `:` in the second axis (1st dimension) selects all rows within each selected 2D block.
   - In this case, it keeps both rows of the selected blocks.

3. **Third part `[-1]`:**
   - The `-1` selects the last element along the third axis (2nd dimension). For each row in the selected blocks, it picks the last element.
   - For example:
     - In the 1st block:
       - From `[ 0,  1,  2,  3,  4]`, it selects `4`.
       - From `[ 5,  6,  7,  8,  9]`, it selects `9`.
     - In the 3rd block:
       - From `[20, 21, 22, 23, 24]`, it selects `24`.
       - From `[25, 26, 27, 28, 29]`, it selects `29`.

### Final result:
The resulting array is:

```python
array([[ 4,  9],
       [24, 29]])
```

### Summary of what `[::2, :, -1]` does:
- `[::2]`: Selects every second block (i.e., the 1st and 3rd blocks).
- `[:, :]`: Keeps all rows from those blocks.
- `[-1]`: Selects the last element of each row in those blocks.

So, the result is the last elements from all rows of the 1st and 3rd 2D sub-arrays.
