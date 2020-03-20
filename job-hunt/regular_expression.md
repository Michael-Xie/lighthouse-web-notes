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
/<expression>/g => g = When a g option (for global) is added to the regular expression, all matches in the string will be replaced, not just the first
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

- usage of /g
- usage of `replace`
```
console.log("Borobudur".replace(/[ou]/, "a"));
// → Barobudur
console.log("Borobudur".replace(/[ou]/g, "a"));
// → Barabadar

console.log(
  "Liskov, Barbara\nMcCarthy, John\nWadler, Philip"
    .replace(/(\w+), (\w+)/g, "$2 $1"));
// → Barbara Liskov
//   John McCarthy
//   Philip Wadler

let s = "the cia and fbi";
console.log(s.replace(/\b(fbi|cia)\b/g,
            str => str.toUpperCase()));
// → the CIA and FBI


let stock = "1 lemon, 2 cabbages, and 101 eggs";
function minusOne(match, amount, unit) {
  amount = Number(amount) - 1;
  if (amount == 1) { // only one left, remove the 's'
    unit = unit.slice(0, unit.length - 1);
  } else if (amount == 0) {
    amount = "no";
  }
  return amount + " " + unit;
}
console.log(stock.replace(/(\d+) (\w+)/g, minusOne));
// → no lemon, 1 cabbage, and 100 eggs


// dynamic creation 
let name = "harry";
let text = "Harry is a suspicious character.";
let regexp = new RegExp("\\b(" + name + ")\\b", "gi");
console.log(text.replace(regexp, "_$1_"));
// → _Harry_ is a suspicious character.
```


- search
```
console.log("  word".search(/\S/));
// → 2 which means the index at which word is found
console.log("    ".search(/\S/));
// → -1  which means not found
```

- sticky vs global
- The difference between the global and the sticky options is that, when sticky is enabled, the match will succeed only if it starts directly at lastIndex, whereas with global, it will search ahead for a position where a match can start.
```
let global = /abc/g;
console.log(global.exec("xyz abc"));
// → ["abc"]
let sticky = /abc/y;
console.log(sticky.exec("xyz abc"));
// → null
```

- looping over matches
- A common thing to do is to scan through all occurrences of a pattern in a string, in a way that gives us access to the match object in the loop body. We can do this by using lastIndex and exec.
```
let input = "A string with 3 numbers in it... 42 and 88.";
let number = /\b\d+\b/g;
let match;
while (match = number.exec(input)) {
  console.log("Found", match[0], "at", match.index);
}
// → Found 3 at 14
//   Found 42 at 33
//   Found 88 at 40
```

- international char
```
console.log(/🍎{3}/.test("🍎🍎🍎"));
// → false
console.log(/<.>/.test("<🌹>"));
// → false
console.log(/<.>/u.test("<🌹>"));
// → true

console.log(/\p{Script=Greek}/u.test("α"));
// → true
console.log(/\p{Script=Arabic}/u.test("α"));
// → false
console.log(/\p{Alphabetic}/u.test("α"));
// → true
console.log(/\p{Alphabetic}/u.test("!"));
// → false
```

- [check over regex](https://debuggex.com )
- [better place to check your work](https://regex101.com/r/sO7zV6/5)

- [source](https://eloquentjavascript.net/09_regexp.html)
