# RESTful

```
// middleware helps keep track and moves on

let numOfVisits = 0;
app.use(req,res,next) => {
	console.log("My middleware runs right now");
	numberOfVisits++;
	next()
})

app.use((req, res, next) => {
	const buffer = [];
	req.on('data', chunk => {
		console.log(chunk);
		buffer.push(chunk);
	}).on('end', () => {
	const str = Buffer.concat(buffer).toString();
	const parsed = str.split("&");
	console.log(parsed);
	const obj = {};
	parsed.forEach(aryg => {
		let keyVal = arg.split("=");
		obj[keyVal[0]] = keyVal[1];
	})
	req.body = obj;
	next();
});

// lets look at req.header

app.use("/urls", (req, res, next) => {
	// check the cookie if the user is logged in,
	// and if the user is logged, and the user exists in the db
	// then next()
	// other redirect("/login")
}

app.use("/urls", (req, res, next) => {
	console.log("This middleware only runs on /urls")
})
```
