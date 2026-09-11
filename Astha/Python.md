## Common Question Patterns

**Array Problems**
    
- Remove duplicates from an array
- Print all duplicates in an array
- Find the largest or smallest element
- Rotate or reverse arrays
    
**String Problems**
    
- Reverse a string
- Check if a string is a palindrome  
- Find the largest word in a string
- Find a substring and its starting position
    
**Number Problems**
    
- Check for leap years
- Count digits or sum of digits
- Factorial or prime number checks
- Number system conversions
    
**Sorting and Searching**

- Implement binary search
- Sort arrays using standard algorithms
- Find kth largest or smallest element
    
**Logical/Pattern Problems**

- Vehicle production problem: calculate two-wheeler and four-wheeler production based on constraints
- Print patterns or validate input constraints


Armstrong number
Prime number
Even odd
Natural number sum 
Sum of up to N numbers
factorial
leap years


Find Largest Element in Array:
```python
# Program to find the maximum element in an array without using max()
def find_max(arr):
  # Initialize the first element as the maximum
  max_value = arr[0] 
  # Iterate through the array

  for num in arr:
    if num > max_value:
      max_value = num # Update max_value if a larger number is found 

  return max_value
# Accept input from the user

array = list(map(int, input("Enter array elements separated by spaces: ").split()))
# Find and display the maximum value
maximum = find_max(array)
print(f"The maximum value in the array is: {maximum}")
```