# Regular Expression

## Creation
```
let re1 = new RegExp("abc");
let re2 = /abc/;
```
## Testing for Matches
```
console.log(/abc/.test("abcde"));
// → true
console.log(/abc/.test("abxde"));
// → false
```
- returns true if pattern occurs anywhere in the string of interest

## Sets of Character
```
[abc] = returns true if string has a, b, or c
[a-z] = returns true if string has any char from a to z
[0-9] = returns true if string has any num from 0 to 9
\d = any digit char
\w = An alphanumeric character (“word character”)
\s = Any whitespace character (space, tab, newline, and similar)
\D = A character that is not a digit
\W = A nonalphanumeric character
\S = A nonwhitespace character
.  = Any character except for newline
[^01] = inverts chars = returns true if string not have 0 or 1
/\d+/ = + means one or more of char 
/\d*/ = * means zero or more of char
/neighbou?r/ = optional pattern to match
/\d{2, 4}/ = must have 2 to 4 digits
/\d{2} = must have 2 digits
(boo)+ = grouped sub-expression to have + apply to more than one element = return true if one or more boo (boo or booboo etc)
/<expression>/i => i = case insensitive
^ - start
$ - end
\b - word boundary char
| - choice between pattern (pig|cow|sheep)s?

```

let match = /\d+/.exec("one two 100");
console.log(match);
// → ["100"]
console.log(match.index);
// → 8

exec returns the match string if it is true, subsequent matches by parentheses are also return
for multiple matches, the last match will be returned
for unfound matches, `undefined` will be returned

```
console.log(/bad(ly)?/.exec("bad"));
// → ["bad", undefined]
console.log(/(\d)+/.exec("123"));
// → ["123", "3"]
```

- can be used to extract specific parts
- note in the example below the Date object has month as zero-indexed that is why you have to minus 1
```
function getDate(string) {
  let [_, month, day, year] =
    /(\d{1,2})-(\d{1,2})-(\d{4})/.exec(string);
  return new Date(year, month - 1, day);
}
console.log(getDate("1-30-2003"));
// → Thu Jan 30 2003 00:00:00 GMT+0100 (CET)
The _ (underscore) binding is ignored and used only to skip the full match element in the array returned by exec.
```
