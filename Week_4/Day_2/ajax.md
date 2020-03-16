# AJAX

- Async JS And XML
- Aside: usual request methods: hyperlink, form

- based on XMLHttpRequest library

## lecture side notes
`app.use(express.static('file))` // load files from that directory

payload = the body or content that is coming back

https://jsonplaceholder.typicode.com/posts
$.getJSON

- success means that there is a response from server, whether failed or not

## cross-site scripting
- code can be inserted by user and executed if used directly in string literal to form the html page
- use jQuery to eliminate this OR use `escape` function around user data
