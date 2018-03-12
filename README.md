# fetch API Example

A modern javascript fetch api example for reference and understanding the working of fetch api.

## What is fetch API?
The Fetch API provides an interface for fetching resources (including across the network). It will seem familiar to anyone who has used XMLHttpRequest, but the new API provides a more powerful and flexible feature set.
_(souce: MDN)_

## ```GET``` Method

GET method is used to retrive data from server.

```js
fetch("https://jsonplaceholder.typicode.com/posts/") // api url to send request
.catch(err => {
	return console.log(err);
})
.then(res => {
	return res.json(); // convert result into json
})
.then(parsedData => {
	return console.log(parsedData); // your response in json
})
```

## ```POST``` Method

POST method is used to send data to server, the code of POST request is same like GET method but an extra data inserted in this request which is require to save or perform a certain operation on server.

```js
fetch("https://jsonplaceholder.typicode.com/posts/", { // api url to send request
	method: "POST",
    body: JSON.stringify({
    	name: 'John Doe',
        email: 'johndoe@email.com'
    }),
    headers: {
    	"Content-Type": "application/json"
    }
}) 
.catch(err => {
	return console.log(err);
})
.then(res => {
	return res.json(); // convert result into json
})
.then(parsedData => {
	return console.log(parsedData); // your response in json
})
```

The fetch api is supports to the modern web browsers.


###### updated on 12 March 2018
