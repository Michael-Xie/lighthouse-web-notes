# Tech Interview
- hackerrank

Starts off
NOTE: tailor to person you are speaking to

1. phone screen
- usually HR
- check out if you are a serial killer
2. Link to hackerrank, codility 
- practise fake question and get feel to how the text editor works

- Cover (insurance tech company)

function romanize(num) {
  const lookup = {
    M: 1000,
    CM: 900,
    D: 500,
    CD: 400,
    C: 100,
    XC: 90,
    L: 50,
    XL: 40,
    X: 10,
    IX: 9,
    V: 5,
    IV: 4,
    I: 1
  };
}
console.log(romanize(123));

123
// look for immediate value less 123
100
// 123 - 100(C) = 23

// look for im less 23
10

// 23 - 10(X)
13

// 13 - 10(X)
3
// 3 - 1(I)
2
// 2 - 1(I)
1
// 1 - 1(I)
0 

function romanize(num) {
	lookup to value immediately less than num
	append lookup key to string
	subtract value of lookup to num
	repeat above step until difference 0 
	if (num === 0) {
		return 
