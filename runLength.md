# Run length: 

## Description:

Given an input string, write a function that returns a compressed version of the string using the Run-length encoding algorithm. This algorithm works by taking the occurrence of each repeating character and outputting that number along with a single character of the repeating sequence. For example: “wwwggopp” would return <code>3w2g1o2p</code>. The string will not contain any numbers, punctuation, or symbols.

<details>
<summary>Solution</summary>
  
```
function runLength(str) {
  let result = '';
  let count = 1;

  for(let i = 0; i < str.length; i++) {
    if(str[i] === str[i+1]) {
      count++;
    } else {
      result += count + str[i];
      count = 1;
    }
  }
  
  return result;
}

console.log(runLength('mmmmaa'));
```

</details>

### Example test cases:

```
mmmmaa = 4m2a
wwooow = 2w3o1w
```
