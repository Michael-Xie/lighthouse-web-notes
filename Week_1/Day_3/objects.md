# Objects

1. Keys are always strings
	- don't need quotes if it doesn't contain spaces, hyphens or periods when assigning or referencing using dot notation
2. Each key is unique
3. Each key is associated with a value. The value can be primitive types or objects

`Object.keys(obj)` returns list of keys of obj
`for ... in` to iterate across the keys of obj
`<obj>.hasOwnProperty(key)` checks to see if key exists in obj
`Object.values(obj)` return list of values of obj

- orders does not matter in objects

when you want to reference another property in the same object, use `this` like `this.driveT`

when passing primitive types to function, it will not be modified. However when passing objects like Array, changes made in function to Array
will be modified (pass by reference).

## Difference between `for .. in` and `for .. of`

### arr
for (i in arr) <--- i index 0, 1,2 arr[i]
for (i of arr) <--- i value at arr

###
