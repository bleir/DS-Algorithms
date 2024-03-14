# Run length: 

## Description:

Given an input string, write a function that returns a compressed version of the string using the Run-length encoding algorithm. This algorithm works by taking the occurrence of each repeating character and outputting that number along with a single character of the repeating sequence. For example: “wwwggopp” would return <code>3w2g1o2p</code>. The string will not contain any numbers, punctuation, or symbols.

<details>
<summary>Solution</summary>
<br>
<style type="text/javascript">
function runLength(str) {
  let result = '';
  let count = 1;
  </code>
  
  <code>for(let i = 0; i < str.length; i++) {
    if(str[i] === str[i+1]) {
      count++;
    } else {
      result += count + str[i];
      count = 1;
    }
  }
  
  return result;
}</style>

<code>console.log(runLength('mmmmaa'))</code>
</details>

### Example test cases:

<i>mmmmaa = 4m2a</i><br>
<i>wwooow = 2w3o1w</i>
