# firstNonRepeated

## Solution code in TypeScript below

```
function firstNonRepeated(s: string): string {
  // make all items in lower case
  const lowerS = s.toLowerCase();

  // create an object to track the frequency of each item in the string
  const freq: Record<string, number> = {};

  // iterate through the string and update the frequency of each item
  for (let i = 0; i < lowerS.length; i++) {
    freq[lowerS[i]] = (freq[lowerS[i]] || 0) + 1;
  }

  // iterate through the string and return the first item with frequency == 1
  for (let i = 0; i < lowerS.length; i++) {
    if (freq[lowerS[i]] === 1) {
      // returns the string in its original case (upper or lower)
      return s[i];
    }
  }

  // else returns an empty string
  return '';
}
```


`
