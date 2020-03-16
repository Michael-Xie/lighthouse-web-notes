# Navigating Rails

- refresh page and see server messages about render
- `raise` to raise an error at section you want to break without using puts or break
	- can use to console.log
	- object`.inspect` turns the object to debug friendly
	- can be used in ERB file to inside <% raise ... %>
- for ERB, can use <%= debug @category %>
	- renders a code tag, yaml serialized object
- use find in projects religiously (cmd shift f)

## Findings
- a ||= b is a conditional assignment operator. It means if a is undefined or falsey, then evaluate b and set a to the result. Equivalently, if a is defined and evaluates to truthy, then b is not evaluated, and no assignment takes place.
https://stackoverflow.com/questions/995593/what-does-or-equals-mean-in-ruby


