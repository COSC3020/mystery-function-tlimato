[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/GDPVb20V)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```


## Step by Step Breakdown:
1) First line just declares a JavaScript function named mystery that takes one parameter a.
   
2) Then the function checks if the length of the array a is equal to 1. If true, array has one element, the function returns that element.

3) If the length of the array is not 1, the function recursively calls itself with a sliced version of the array where said slice is a truncated version of the array with the first element removed.
It creates a new variable foo to store the final value of the recursive call.

4) After the recursive call, check if foo is greater than the first element of the input array. If true, it returns foo.

6) if false, then the first element of the original input array is greater than or equal to the result of the recursive call, and the first element is returned.


### References:
https://www.w3schools.com/jsref/jsref_slice_array.asp
