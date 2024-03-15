# First Factorial: 

## Description:

Have the function <code>FirstFactorial(num)</code> take the <code>num</code> parameter being passed and return the factorial of it. For example: if <code>num</code> = 4, then your program should return <code>(4 * 3 * 2 * 1)</code> = 24. For the test cases, the range will be between 1 and 18 and the input will always be an integer.

<details>
<summary>Solution</summary>

```
  function FirstFactorial(num) {
    return num === 1 ? 1 : num * FirstFactorial(num - 1);
  }
  
  console.log(FirstFactorial(8));
```
</details>

### Example test cases:

```
4! = 4 × 3 × 2 × 1 = 24
7! = 7 × 6 × 5 × 4 × 3 × 2 × 1 = 5040
1! = 1
```
