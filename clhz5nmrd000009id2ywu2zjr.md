---
title: "Cookbook #1: Making a website that talks to an API is surprisingly easy."
datePublished: Mon May 22 2023 18:02:42 GMT+0000 (Coordinated Universal Time)
cuid: clhz5nmrd000009id2ywu2zjr
slug: cookbook1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684778709402/09b9abe8-5e96-458f-bfa3-2cb37d364398.png
tags: css, javascript, apis, html5, wemakedevs

---

Let's create a website that integrates an API to show useful information such as the weather. Here's a comprehensive guide with simplified steps that any beginner can follow along.

## Ingredients:

* HTML/CSS for the webpage
    
* JavaScript for talking to the API
    
* [VSCode](https://code.visualstudio.com/download) or Code Editor of your choice
    
* [WeatherAPI](https://www.weatherapi.com/) is the API we'll use
    
* [Postman](https://www.postman.com/) to test the API
    

## The Steps:

### Set up your editor and files

We'll begin by creating a new project in your Code Editor.

1. For VSCode users, Head over to **Explorer -&gt; Open Folder -&gt; (Open your Desired folder or create a new folder).**
    
2. Go to **File -&gt; New File**. We'll name this file `index.html`.
    

### Set up your account on WeatherAPI Website

Creating an account on WeatherAPI is very easy. Just SignUp at the HomePage and enter your email id and set a password. An API key will automatically be created for you which will be available in your [Account Page](https://www.weatherapi.com/my/).

An application programming interface (API) key is **a code used to identify and authenticate an application or user**. It is unique to your account.

To know more about APIs in general, please read my [previous blog post](https://himanshubalani.hashnode.dev/the-ins-and-outs-of-apis).

> ***⚠️ It is very important that you keep your API key private and not share it with others for privacy and to avoid potential misuse of your API account. ⚠️***

Read [WeatherAPI docs](https://www.weatherapi.com/docs/) to know all about their service.

### Begin Coding 🚥

1. You have already made index.html. Let's start by typing some code in it.
    

> 💡Tip: Type `doc` and press enter to create boiler code for HTML.

```xml
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Weather Website</title>
</head>
<body>
	
</body>
</html>
```

1. Let's start by adding a heading and a form to input data.
    

```html
	<h1 class="text-center">Weather</h1>
	<form >
		<input id="cityname" type="text" placeholder="Enter City Name">
		<button id="search" type="button" class="btn btn-outline-primary">Search</button>
	</form>
```

1. Add temperature card.
    
    ```html
    <div class="card">
        <div class="temperature-container">
    	    <p class="text-left">Current Temperature:</p>
    		<p class="text-right" id="currtemp"></p>
    	</div
    </div
    ```
    
2. Repeat the code to add Condition and Windspeed.
    

We then wrap this in a section to make it pretty later.

Here's the entire HTML file.

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link href="style.css" rel="stylesheet">
	<title>Weather</title>
</head>
<body>
	<section>
		<div class="container">
			<div class="name">
				<h1 class="text-center">Weather</h1>
			</div>
			<div class="card">
				<form>
					<input id="cityname" type="text" placeholder="Enter City Name">
					<button id="search" type="button" class="btn">Search</button>
				</form>
				<div class="card">
					<div class="temperature-container">
						<p class="text-left">Current Temperature:</p>
						<p class="text-right" id="currtemp"></p>
					</div>
				</div>
				<div class="card">
					<div class="temperature-container">
						<p class="text-left">Condition:</p>
						<p class="text-right" id="condition"></p>
					</div>
				</div>
				<div class="card">
					<div class="temperature-container">
							<p class="text-left">WindSpeed:</p>
							<div class="temperature-container">
								<p class="text-right" id="windspeed"></p>
							</div>
					</div>
				</div>
			</div>
		</div>
	</section>

//Scripts
	<script type='text/javascript' src='config.js'></script>
	<script type='text/javascript' src="index.js"></script>
</body>
</html>
```

### Add some style 🤵🏻

You can learn all about CSS from [W3Schools](https://www.w3schools.com/css/). Create a new file called `style.css`. This is the Stylesheet we'll use for styling the website.

```css
body {
    font-family: Arial, sans-serif;
    background-color: #C1CFEA;
    margin: 0;
    padding: 0;
}

.container {
    max-width: 600px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
}

h1 {
    color: #333;
    margin-top: 0;
}

sup {

	color: #333;
	margin-left: 3.5px;
}

p {
	font-weight:lighter;
	color: #333;
	margin-top: 0;
}

form {
    margin-bottom: 20px;
}

input[type="text"] {
	background-color: #fff;
    width: 80%;
    padding: 10px;
    border-radius: 5px;
    border: none;
    outline: none;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

button {
	margin-top: 5%;
    width: 100%;
    padding: 10px;
    border: none;
    border-radius: 5px;
    background-color: #007bff;
    color: #fff;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

.card {
	margin: 5px;
    background-color: #fff;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}

.temperature-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.temperature-container p {
    margin: 0;
}

.text-left {
    text-align: left;
}

.text-right {
    text-align: right;
}

@media (max-width: 768px) {
    .container {
        padding: 10px;
    }
}
```

The website looks like this now.👇🏻

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684780472607/a5dbaa42-9867-4e91-a1b5-0f3cd12f7254.png align="center")

  

### Let's call the API to know what it's up to 📞

Go to [Postman](https://www.postman.com/) and create an account. Once you do that, you can see a space to enter our URL to call the API beside **GET**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684769093007/731ea4d3-7d47-4280-b214-9457782e80ad.png align="center")

Before entering the URL let's secure your API key in Postman.

1. Click on **Enviroment Quick Look (it's an icon)** beside "No Enviroment" and we'll add your API key.
    
    1. Click on **Edit** to add your apikey.
        
    2. The variable name could be anything but we'll try with `apikey`.
        
    3. The type is `default`.
        
    4. Initial Value is your API key from weatherapi.com
        
    5. Click on 💾Save.
        
2. Now back to entering the URL. Enter this👇🏻
    
    1. `https://api.weatherapi.com/v1/current.json?key={{apikey}}&q=Bangalore&days=3&aqi=yes&alerts=no`
        
    2. The q is the query and the name of the place you're trying to get Weather from.
        
3. Click "Send"
    
4. A response appears. Or an Error. If former, Congrats! the API works. You can experiment with it using the documentation to see different results.
    

Let's use this URL on our website now.

### Sprinkle some logic into our website ✨

We should probably safeguard the API key by creating a separate file to store it and call it from there.

Create a New File called `config.js` in the same folder and add the code below.

```javascript
var config = {
	apikey: "<YOUR_API_KEY>",
};
```

Replace `<YOUR_API_KEY>` with your API key.

Let's now create a Javascript file that'll serve as the logic that calls the API and retrieves the weather data.

1. We begin by calling the API when the User clicks on submit.
    
    ```javascript
    document.getElementById("search").addEventListener("click", apicall);
    ```
    
    This line of code uses the `addEventListener()` method to attach the `apicall()` function to the click event of the element with the ID "search." This means that whenever the user clicks on the element with the ID "search," the `apicall()` function will be called.
    
2. Let's create the `apicall()` function.
    
    ```javascript
    function apicall() {}
    ```
    
3. Declare the variables.
    
    ```javascript
    const apikey = config.apikey;
    const cityname = document.getElementById("cityname").value;
    const url = `https://api.weatherapi.com/v1/current.json?key=${apikey}&q=${cityname}&days=3&aqi=yes&alerts=no`;
    ```
    
    These lines of code construct a URL for the API call. The URL includes the API key, city name, and other parameters. The `day` parameter specifies the number of days of weather data to return. The `aqi` parameter specifies whether to return air quality index data. The `alerts` parameter specifies whether to return alert data.
    
4. The `fetch()` function.
    
    ```javascript
    fetch(url)
    .then((response) => response.json())
    .then((data) => {}
    ```
    
    This line of code uses the `fetch()` function to send a GET request to the specified URL. The `fetch()` function returns a Promise that resolves to the response from the server. The next `.then()` block is called when the Promise is fulfilled.
    
5. Parsing the Output
    
    ```javascript
    let currtemp = `
    <div> 
    <p>${data.current.temp_c}<sup>℃</p>
    </div>`
    ;
    document.getElementById("currtemp").innerHTML = currtemp;
    ```
    
    This line of code creates an HTML string output containing the temperature value from the received data. The `data` object contains the weather data for the city that the user requested. The `current` property of the `data` object contains the current weather conditions for the city. The `temp_c` property of the `current` object contains the current temperature in degrees Celsius.
    
6. We repeat this step to get other data like **Condition** and **Windspeed**.
    
7. Error checking
    
    ```javascript
    }).catch((err) => console.log(err));
    ```
    
    This line of code catches any errors that occur during the process and logs the error message to the console.
    

The Entire `index.js` file is given below.

```javascript
document.getElementById("search").addEventListener("click", apicall);

function apicall() {
	const apikey = config.apikey;
	const cityname = document.getElementById("cityname").value;
  	const url = `https://api.weatherapi.com/v1/current.json?key=${apikey}&q=${cityname}&days=3&aqi=yes&alerts=no`;
  	fetch(url)
	.then((response) => response.json())
	.then((data) => {
	  	let currtemp = `
	  	<div> 
			<p>${data.current.temp_c}<sup>℃</p>
	  	</div>`
	;
	  	document.getElementById("currtemp").innerHTML = currtemp;
		let condition = `
		<div>
			<p>${data.current.condition.text}</p>
		</div>`
	;
	document.getElementById("condition").innerHTML = condition;
	let windspeed = `
		<div>
			<p>${data.current.wind_kph}<sup>kmph</p>
		</div>`
	;
	document.getElementById("windspeed").innerHTML = windspeed;
		}).catch((err) => console.log(err));
}
```

### The meal is prepared, garnish with creativity.

You can experiment with additional data like adding multiple-day forecasts or Air Quality Index.

You can check out my entire code from my GitHub repository [here](https://github.com/himanshubalani/weather). The website works like this.  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684781309539/9794d3aa-afc1-4ed9-b575-5324d40ec628.gif align="center")

Congrats on making it this far! Hope this tutorial helped you get started with your API journey.

Thank you for reading 💓, please like my blog which keeps me motivated to write more content, and also don't forget to leave your views down below 👇.

Here have a cookie 🍪.

---

*This blog is part of the* [*WeMakeDevs X Hashnode*](https://wemakedevs.org/events/hashnode) *Blogging Challenge. They provide amazing prizes for winners. Do check 'em out. I'm participating in the Development track.*