# Array Addition: 

## Description:

Using the JavaScript language, have the function ArrayAdditionI(arr) take the array of numbers stored in arr and return the string true if any combination of numbers in the array can be added up to equal the largest number in the array, otherwise return the string false. For example: if arr contains [4, 6, 23, 10, 1, 3] the output should return true because 4 + 6 + 10 + 3 = 23. The array will not be empty, will not contain all the same elements, and may contain negative numbers.

<details>
<summary>Solution</summary>
<br>
<code>function ArrayAddition(arr) {
  const biggestNumber = arr.sort((a,b) => a - b)[arr.length-1];
  const restElements = arr.splice(0, arr.length - 1);
  <br>  
  return restElements.reduce((acc, item) => acc + item, 0) === biggestNumber;
}
<br><br>
console.log(ArrayAddition([1, 3, 8, 5, 17]));</code>
</details>

### Example test cases:


<i>[1, 3, 8, 5, 17] = true</i><br>
<i>[4, 8, 22, 2, 3] = false</i>
