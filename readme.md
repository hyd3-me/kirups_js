
2 head. variable

переменные не могут начинаться с чисел.
могут содержать любое количсество символов.
не могут содержать пробельный символ.

name validator link follow:
https://mothereff.in/js-variables

const varName ; - объявление константы.

head4

изучаем оператор if / else
if (condition) {
doSomth();
}
else if (condition) {
doSomth2();
}
else {
}


perator switch/case

switch (color) {
case 'green':
	alert('green');
	break;
case 'red':
	alert('red');
	break;
default:
	alert('default');
	break
}


** head5 cycle

* for

for (let i = 0; i < 10; i++) {
saySomething();
}

let i = 0;
let yay = true;
for (; yay;) {
if (i == 10) {
yay = false;
} else {
i++;
document.writeln("weird");
}
}

head 6
# comments in code

комментарии важная часть работы с кодом.
со временем забывается, что делает код. важно кратко описывать основную суть.
комментарии раскрывают свою пользу со временем. комментарии должны кратко описывать работу программы человеческим языком.


head7
# timers

вызывает функцию через указанное в млсекундах время.
let timeoutID = setTimeout(func, 5000);
clearTimeout(timeoutID);


let intervalID = setInterval(func, 3000);
clearInterval(intervalID);

let requestID = requestAnimationFrame(func);


head8
#variable scop

объявление переменной без использования let делает ее глобальной

дочерние блокие кода имеют доступ к области видимости переменных своих родителей. а родители не имеют доступа к области видимости дочерних блоков.

var - делает переменную доступной на уровне функции.

head9
#closures

function stopWatch() {
let startTime = Date.now();
function getDelay() {
let elapsedTime = Date.now() — startTime;
alert(elapsedTime);
}
return getDelay;
}


head10
# js code placement

head11
#console

console.log('text');
console.warn('text');
console.error('text'); // plus tracert

head12
#types

head13
#array

let groceries = [];
let groceries = ["Milk", "Eggs", "Frosted Flakes", "Salami", "Juice"];

for (let i = 0; i < groceries.length; i++) {
let item = groceries[i];
}

groceries.push("Cookies");
groceries.unshift("Bananas");

let lastItem = groceries.pop();
let firstItem = groceries.shift();

#search
indexOf, lastIndexOf, includes, find, findIndex и filter

let groceries = ["Milk", "Eggs", "Frosted Flakes", "Salami", "Juice"];
let resultIndex = groceries.indexOf("Eggs",0); // elem + start index
console.log(resultIndex); // 1

Если же искомый элемент в массиве отсутствует, оба этих метода
возвращают -1.

let good = ["Mario", "Luigi", "Kirby", "Yoshi"];
let bad = ["Bowser", "Koopa Troopa", "Goomba"];
let goodAndBad = good.concat(bad);
console.log(goodAndBad);

let names = ["marge", "homer", "bart", "lisa", "maggie"];
let newNames = [];
for (let i = 0; i < names.length; i++) {
	let name = names[i];
	let firstLetter = name.charAt(0).toUpperCase();
	newNames.push(firstLetter + name.slice(1));
}
console.log(newNames);

let newArray = originalArray.map(someFunction);

let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12];
let evenNumbers = numbers.filter(function (item) {
return (item % 2 == 0);
});
console.log(evenNumbers);

let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12];
let total = numbers.reduce(function(total, current) {
return total + current;
}, 0);

head14
#string

let text = "this is some text";
let moreText = 'I am in single quotes!';

let initial = "hello";
console.log(initial + " world!");
console.log("I can also " + "do this!");

let vowels = "aeiou";
console.log(vowels[2]);

let vowels = "aeiou";
for (let i = 0; i < vowels.length; i++) {
console.log(vowels[i]);
}

let vowels = "aeiou";
console.log(vowels.charAt(2));

let textA = "Please";
let textB = new String("stop!");
let combined = textA + " make it " + textB;
console.log(combined);

# slice
let theBigString = "Pulp Fiction is an awesome movie!";
console.log(theBigString.slice(5, 12));

let theBigString = "Pulp Fiction is an awesome movie!";
console.log(theBigString.slice(0, -6));

let theBigString = "Pulp Fiction is an awesome movie!";
console.log(theBigString.slice(-14, -7));

# substr
let theBigString = "Pulp Fiction is an awesome movie!";
console.log(theBigString.substr(0, 4)); // Pulp

let theBigString = "Pulp Fiction is an awesome movie!";
console.log(theBigString.substr(5, 7)); // Fictiona

let theBigString = "Pulp Fiction is an awesome movie!";
console.log(theBigString.substr(5)); // Fiction is an awesome movie!

# split
let inspirationalQuote = "That which you can concatenate, you can
also split apart.";
let splitWords = inspirationalQuote.split(" ");
console.log(splitWords.length); // 10

let days = "Monday,Tuesday,Wednesday,Thursday,Friday, Saturday,Sunday";
let splitWords = days.split(",");
console.log(splitWords[6]); // Sunday

let question = "I wonder what the pigs did to make these birds so
angry?";
console.log(question.indexOf("pigs")); // 18

let question = "I wonder what the pigs did to make these birds so
angry?";
console.log(question.indexOf("z")); // -1

let question = "How much wood could a woodchuck chuck if
a woodchuck could chuck wood?";
console.log(question.lastIndexOf("wood")); // 65

let question = "How much wood could a woodchuck chuck if
a woodchuck could chuck wood?";
console.log(question.indexOf("wood", 30)); // 43

let phrase = "There are 3 little pigs.";
let regexp = /[0-9]/;
let numbers = phrase.match(regexp);
console.log(numbers[0]); // 3

let phrase = "My name is Bond. James Bond.";
console.log(phrase.toUpperCase()); // MY NAME IS BOND. JAMES BOND.
console.log(phrase.toLowerCase()); // my name is bond. james bond.


head 15

let greeting = "Hi, everybody!!!";
let shout = greeting.toUpperCase();

let game = "Dragon Age: Origins";
console.log("Length is: " + game.length);
let gameObject = new String("Dragon Age:Origins");
console.log(typeof game); // строка
console.log(typeof game.length); // число
console.log(typeof gameObject); // объект


head 16 numbers

let pi = 3.14159;
let color = 0xFF;
let massOfEarth = 5.9742e+24;

let temperature = -42;

#operatotors
let total = 4 + 26;
let average = total / 2;
let doublePi = 2*3.14159;
let subtractItem = 50 — 25;
let remainder = total % 7;
let more = (1 + average * 10) / 5;

# oct
let leet = 0o2471;
# hex
let leet = 0x539;

let myLoveForYou = Infinity * 2;
let nope = 1920 / "blah";

# Math
Math.E
Math.LN2
Math.LN10
Math.LOG2E
Math.LOG10E
Math.PI
Math.SQRT1_2
Math.SQRT2

function getCircumference(radius) {
return 2 * Math.PI * radius;
}
console.log(getCircumference(2));

Math.floor(.5); // 0
Math.ceil(.5); // 1
Math.round(.5); // 1
Math.floor(3.14); // 3
Math.round(3.14); // 3
Math.ceil(3.14); // 4
Math.floor(5.9); // 5
Math.round(5.9); // 6
Math.ceil(5.9); // 6

Math.cos(0); // 1
Math.sin(0); // 0
Math.tan(Math.PI / 4); // 1
Math.cos(Math.PI); // 1
Math.cos(4 * Math.PI); // 1

Math.pow(2, 4); //эквивалент 2^4 (или 2 * 2 * 2 * 2)
Math.exp(3); //эквивалент Math.E^3
Math.sqrt(16); //4

Math.abs(37); //37
Math.abs(-6); //6

let randomNumber = Math.random() * 100;

# head 17 props

let foo = {
a: "Hello",
b: "Monday";
}
console.log(foo.a);

let zorb = {
message: "Blah",
get greeting() {
return this.message;
},
set greeting(value) {
this.message = value;
}
};

var shout = {
_message: "HELLO!",
get message() {
return this._message;
},
set message(value) {
this._message = value.toUpperCase();
}
};
shout.message = "This is sparta!";
console.log(shout.message);

var superSecureTerminal = {
allUserNames: [],
_username: "",
showHistory() {
console.log(this.allUserNames);
},
get username() {
return this._username;
},
set username(name) {
this._username = name;
this.allUserNames.push(name);
}
}

var myTerminal = Object.create(superSecureTerminal);
myTerminal.username = "Michael Gary Scott";
myTerminal.username = "Dwight K. Schrute";
myTerminal.username = "Creed Bratton";
myTerminal.username = "Pam Beasley";
myTerminal.showHistory();

let person = {
_name: "",
_age: "",
get name() {
return this._name;
},
set name(value) {
if (value.length > 2) {
this._name = value;
} else {
	console.log("Name is too short!");
}
},
get age() {
return this._age;
},
set age(value) {
if (value < 5) {
console.log("Too young!");
} else {
this._age = value;
}
},
get details() {
return "Name: " + this.name + ", Age: " + this.age;
}
}


# head 18 Objects

let funnyGuy = {};
funnyGuy.firstName = "Conan";
let funnyFirstName = funnyGuy.firstName;

## alternaative way
funnyGuy["firstName"] = "Conan";
funnyGuy["lastName"] = "O'Brien";

let myObject = {};
for (let i = 0; i < 5; i++) {
let propertyName = "data" + i;
myObject[propertyName] = Math.random() * 100;
}

let funnyGuy = {
firstName: "Conan",
lastName: "O'Brien"
};

let colors = {
header: "blue",
footer: "gray",
content: {
title: "black",
body: "darkgray",
signature: "light blue"
}
};

## remove props

delete colors.footer;
// или
delete colors["footer"];

colors.footer = undefined;
// или
colors["footer"] = undefined;

let funnyGuy = {};
funnyGuy.toString(); // [объект Object]

## prototype

let person = {
getName: function () {
return "The name is " + this.firstName + " " + this.lastName;
}
};
let funnyGuy = Object.create(person);
funnyGuy.firstName = "Conan";
funnyGuy.lastName = "O'Brien";
let theDude = Object.create(person);
theDude.firstName = "Jeffrey";
theDude.lastName = "Lebowski";
let detective = Object.create(person);
detective.firstName = "Adrian";
detective.lastName = "Monk";

detective.getName(); // Имя Adrian Monk

let person = {
getName: function () {
return "The name is " + this.firstName + " " + this.lastName;
},
getInitials: function () {
if (this.firstName && this.lastName) {
return this.firstName[0] + this.lastName[0];
}
}
};

funnyGuy.getInitials(); // CO

let spaceGuy = Object.create(person);
spaceGuy.firstName = "Buzz";
spaceGuy.lastName = "Lightyear";
console.log(spaceGuy.getName()); // Buzz Lightyear

# head 19 extands base Objecst

function shuffle(input) {
for (let i = input.length — 1; i >= 0; i--) {
let randomIndex = Math.floor(Math.random() * (i + 1));
let itemAtIndex = input[randomIndex];
input[randomIndex] = input[i];
input[i] = itemAtIndex;
}
return input;
}

Array.prototype.shuffle = function () {
let input = this;
for (let i = input.length — 1; i >= 0; i--) {
let randomIndex = Math.floor(Math.random() * (i + 1));
let itemAtIndex = input[randomIndex];
input[randomIndex] = input[i];
input[i] = itemAtIndex;
}
return input;
}

let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
numbers.shuffle();

Array.prototype.slice = function () {
let input = this;
input[0] = "This is an awesome example!";
return input;
}
let tempArray = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
tempArray.slice();
// и результат будет...
console.log(tempArray);


# head 20 classes

class Planet {
}
let myPlanet = new Planet();

## constructor

class Planet {
constructor(name, radius) {
this.name = name;
this.radius = radius;
}
}

let myPlanet = new Planet("Earth", 6378);
console.log(myPlanet.name); // Earth

function Planet(name, radius) {
this.name = name;
this.radius = radius;

};
let myPlanet = new Planet("Earth", 6378);
console.log(myPlanet.name); // Earth

class Planet {
constructor(name, radius) {
this.name = name;
this.radius = radius;
}
getSurfaceArea() {
let surfaceArea = 4 * Math.PI * Math.pow(this.radius, 2);
console.log(surfaceArea + " square km!");
return surfaceArea;
}
}

let earth = new Planet("Earth", 6378);
earth.getSurfaceArea();

class Planet {
constructor(name, radius) {
this.name = name;
this.radius = radius;
}
getSurfaceArea() {
let surfaceArea = 4 * Math.PI * Math.pow(this.radius, 2);
console.log(surfaceArea + " square km!");
return surfaceArea;
}
set gravity(value) {
console.log("Setting value!");
this._gravity = value;
}
get gravity() {
console.log("Getting value!");
return this._gravity;
}
}
let earth = new Planet("Earth", 6378);
earth.gravity = 9.81;
earth.getSurfaceArea();
console.log(earth.gravity) // 9.81

## extends objects

class PotatoPlanet {
constructor(name, radius, potatoType) {
this.name = name;
this.radius = radius;
this.potatoType = potatoType;
}
getSurfaceArea() {
let surfaceArea = 4 * Math.PI * Math.pow(this.radius, 2);
console.log(surfaceArea + " square km!");
return surfaceArea;
}
getPotatoType() {
var thePotato = this.potatoType.toUpperCase() + "!!1!!!";
console.log(thePotato);
return thePotato;
}
set gravity(value) {
console.log("Setting value!");
this._gravity = value;
}
get gravity() {
return this._gravity;
}
}

class Planet {
constructor(name, radius) {
this.name = name;
this.radius = radius;
}
getSurfaceArea() {
let surfaceArea = 4 * Math.PI * Math.pow(this.radius, 2);
console.log(surfaceArea + " square km!");
return surfaceArea;
}
set gravity(value) {
console.log("Setting value!");
this._gravity = value;
}
get gravity() {
return this._gravity;
}
}
class PotatoPlanet extends Planet {
constructor(name, width, potatoType) {
super(name, width);
this.potatoType = potatoType;
}
getPotatoType() {
let thePotato = this.potatoType.toUpperCase() + "!!1!!!";
console.log(thePotato);
return thePotato;
}
}


# head 21 logic operators

## boolean

let sunny = false;
let traffic = true;

let boolObject = new Boolean(false);
let anotherBool = new Boolean(true);

let bool;
bool = Boolean(null);
bool = Boolean(undefined);
bool = Boolean();
bool = Boolean(0);
bool = Boolean("");
bool = Boolean(false);

let bool;
bool = Boolean(true);
bool = Boolean("hello");
bool = Boolean(new Boolean()); // Внедрение!!!
bool = Boolean("false"); // "false" — это строка
bool = Boolean({});
bool = Boolean(3.14);
bool = Boolean(["a", "b", "c"]);

let boolObject = new Boolean(false);
if (boolObject) {
console.log("Bool, you so crazy!!!");
}

## Strict inequality (!==)

// true
function theSolution(answer) {
if (answer == 42) {
console.log("You have nothing more to learn!");
}
}
theSolution("42"); // 42 передано как строка

// false
function theSolution(answer) {
if (answer === 42) {
console.log("You have nothing more to learn!");
}
}
theSolution("42"); // 42 передано как строка

// all false
console.log(new String("A") == new String("A"));
console.log([1, 2, 3] == [1, 2, 3]);
console.log({ a: 1 } == { a: 1 });

# head 22. null, undefined

let name = null;
if (name === null) {
name = "Peter Griffin";
} else {
name = "No name";
}

let myVariable;
console.log(myVariable); // undefined
function doNothing() {
// watch paint dry
return;
}

let weekendPlans = doNothing();
console.log(weekendPlans); // undefined
let person = {
firstName: "Isaac",
lastName: "Newton"
}
console.log(person.title); // undefined

if (myVariable === undefined) {
// делает что-нибудь
}

let myVariable;
if (typeof myVariable === "undefined") {
console.log("Define me!!!");
}

# JSON

let funnyGuy = {
firstName: "Conan",
lastName: "O'Brien",
getName: function () {
return "Name is: " + this.firstName + " " + this.lastName;
}
};
let theDude = {
firstName: "Jeffrey",
lastName: "Lebowski",
getName: function () {
return "Name is: " + this.firstName + " " + this.lastName;
}
};
let detective = {
firstName: "Adrian",
lastName: "Monk",
getName: function () {
return "Name is: " + this.firstName + " " + this.lastName;
}
};

{
"response": {
"version": "0.1",
"termsofService":
"http://www.wunderground.com/weather/api/d/terms.html",
"features": {
"conditions": 1
}
},
"current_observation": {
"image": {
"url": "http://icons.wxug.com/graphics/wu2/logo_130x80.png",
"title": "Weather Underground",
"link": "http://www.wunderground.com"
},
"display_location": {
"full": "Seattle, WA",
"city": "Seattle",
"state": "WA",
"state_name": "Washington",
"country": "US",
"country_iso3166": "US",
"zip": "98101",
"magic": "1",
"wmo": "99999",
"latitude": "47.61167908",
"longitude": "-122.33325958",
"elevation": "63.00000000"
},
"observation_location": {
"full": "Herrera, Inc., Seattle, Washington",
"city": "Herrera, Inc., Seattle",
"state": "Washington",
"country": "US",
"country_iso3166": "US",
"latitude": "47.616558",
"longitude": "-122.341240",
"elevation": "121 ft"
},
"estimated": {},
"station_id": "KWASEATT187",
"observation_time": "Last Updated on August 28, 9:28 PM PDT",
"observation_time_rfc822": "Fri, 28 Aug 2015 21:28:12 -0700",
"observation_epoch": "1440822492",
"local_time_rfc822": "Fri, 28 Aug 2015 21:28:45 -0700",
"local_epoch": "1440822525",
"local_tz_short": "PDT",
"local_tz_long": "America/Los_Angeles",
"local_tz_offset": "-0700",
"weather": "Overcast",
"temperature_string": "68.0 F (20.0 C)",
"temp_f": 68.0,
"temp_c": 20.0,
"relative_humidity": "71%",
"wind_string": "Calm",
"wind_dir": "NNW",
"wind_degrees": 331,
"wind_mph": 0.0,
"wind_gust_mph": "10.0",
"wind_kph": 0,
"wind_gust_kph": "16.1",
"pressure_mb": "1008",
"pressure_in": "29.78",
"pressure_trend": "-",
"dewpoint_string": "58 F (15 C)",
"dewpoint_f": 58,
"dewpoint_c": 15,
"heat_index_string": "NA",
"heat_index_f": "NA",
"heat_index_c": "NA",
"windchill_string": "NA",
"windchill_f": "NA",
"windchill_c": "NA",
"feelslike_string": "68.0 F (20.0 C)",
"feelslike_f": "68.0",
"feelslike_c": "20.0",
"visibility_mi": "10.0",
"visibility_km": "16.1",
"solarradiation": "--",
"UV": "0",
"precip_1hr_string": "0.00 in ( 0 mm)",
"precip_1hr_in": "0.00",
"precip_1hr_metric": " 0",
"precip_today_string": "0.00 in (0 mm)",
"precip_today_in": "0.00",
"precip_today_metric": "0",
"icon": "cloudy",
"icon_url": "http://icons.wxug.com/i/c/k/nt_cloudy.gif",
"nowcast": ""
}
}

{
"firstName": "Kirupa",
"lastName": "Chinnathambi",
"special": {
"admin": true,
"userID": 203
},
"devices": [
{
"type": "laptop",
"model": "Macbook Pro 2015"
},
{
"type": "phone",
"model": "iPhone 6"
}
]
}

let exampleJSON = {
"firstName": "Kirupa",
"lastName": "Chinnathambi",
"special": {
"admin": true,
"userID": 203
},
"devices": [
{
"type": "laptop",
"model": "Macbook Pro"
},
{
"type": "phone",
"model": "iPhone XS"
}
]
};

exampleJSON.firstName;
exampleJSON["firstName"];
exampleJSON.special.userID;
exampleJSON.devices[0].model;

let devicesArray = exampleJSON.devices;
for (let i = 0; i < devicesArray.length; i++) {
let type = devicesArray[i].type;
let model = devicesArray[i].model;
// Делает что-нибудь интересное с этими данными.
}

function processRequest(e) {
if (xhr.readyState == 4 && xhr.status == 200) {
let response = JSON.parse(xhr.responseText);
selectInitialState(response.region);
}
}


# head 24. js, DOM, HTML, CSS

## html

<!DOCTYPE html>
<html>
<head>
<meta content="sea otter, kid, stuff" name="keywords">
<meta content="Sometimes, sea otters are awesome!"
name="description">
<title>Example</title>
<link href="foo.css" rel="stylesheet" />
</head>
<body>
<div id="container">
<img src="seaOtter.png" />
<h1>What This Sea Otter Did to This Little Kid Will Make You
LOL!</h1>
<p class="bodyText">
Nulla tristique, justo eget semper viverra,
massa arcu congue tortor, ut vehicula urna mi
in lorem. Quisque aliquam molestie dui, at tempor
turpis porttitor nec. Aenean id interdum urna.
Curabitur mi ligula, hendrerit at semper sed,
feugiat a nisi.
</p>
<div class="submitButton">
more
</div>
</div>
<script src="stuff.js"></script>
</body>
</html>

## CSS

body {
font-family: "Arial";
background-color: #CCCFFF;
}
#container {
margin-left: 30%;
}
#container img {
padding: 20px;
}
#container h1 {
font-size: 56px;
font-weight: 500;
}
#container p.bodyText {
font-size: 16px;
line-height: 24px;
}
.submitButton {
display: inline-block;
border: 5px solid #669900;
background-color: #7BB700;
padding: 10px;
width: 150px;
font-weight: 800;
}


# head 25: Dive into DOM

## querySelector

<div id="main">
<div class="pictureContainer">
<img class="theImage" src="smiley.png" height="300" width="150" />
</div>
<div class="pictureContainer">
<img class="theImage" src="tongue.png" height="300" width="150" />
</div>
<div class="pictureContainer">
<img class="theImage" src="meh.png" height="300" width="150" />
</div>
<div class="pictureContainer">
<img class="theImage" src="sad.png" height="300" width="150" />
</div>
</div>

let element = document.querySelector("CSS selector");
let element = document.querySelector("#main");
let element = document.querySelector(".pictureContainer");

let elements = document.querySelectorAll("CSS selector");

let images = document.querySelectorAll(".theImage");
for (let i = 0; i < images.length; i++) {
let image = images[i];
console.log(image.getAttribute("src"));
}

## CSS

let images = document.querySelectorAll("img");
let images = document.querySelectorAll("img[src='meh.png']");

# head 26: DOM modifyication

<!DOCTYPE html>
<html>
<head>
<title>Hello...</title>
<style>
.highlight {
font-family: "Arial";
padding: 30px;
}
.summer {
font-size: 64px;
color: #0099FF;
}
</style>
</head>
<body>
<h1 id="bigMessage" class="highlight summer">What's happening?</h1>
<script>
</script>
</body>
</html>

## textCntent
<script>
    let headingElement = document.querySelector("#bigMessage");
    headingElement.textContent = "Oppa Gangnam Style!";
</script>

<img src="images/lol_panda.png" alt="Sneezing Panda!"/>
<img src="images/cat_cardboard.png" alt="Cat sliding into box!"/>
<img src="images/dog_tail.png" alt="Dog chasing its tail!"/>

## getAttribure
<body>
<h1 id="bigMessage" class="highlight summer">What's happening?</h1>
<script>
let headingElement = document.querySelector("h1");
console.log(headingElement.getAttribute("id")); // bigMessage
</script>
</body>

## setAttribute
<body>
<h1 id="bigMessage" class="highlight summer">What's happening?</h1>
<script>
let headingElement = document.querySelector("h1");
headingElement.setAttribute("class", "bar foo");
</script>
</body>

<body>
<h1 id="bigMessage" class="highlight summer">What's happening?</h1>
<script>
let headingElement = document.querySelector("h1");
console.log(headingElement.id); // bigMessage
headingElement.className = "bar foo";
</script>
</body>

# head 27 CSS

let myElement = document.querySelector("#superman");
myElement.style.backgroundColor = "#D93600";

myElement.style.transform = "translate3d(" + xPos + ", " + yPos + "px, 0)";
myElement.style.transform = `translate3d(${xPos}px, ${yPos}px, 0)`;


.disableMenu
{ display: none;
}

<ul id="dropDown">
<li>One</li>
<li>Two</li>
<li>Three</li>
<li>Four</li>
<li>Five</li>
<li>Six</li>
</ul>

<ul class="disableMenu" id="dropDown">
<li>One</li>
<li>Two</li>
<li>Three</li>
<li>Four</li>
<li>Five</li>
<li>Six</li>
</ul>

classList:
- add;
- remove;
- toggle;
- contains.

let divElement = document.querySelector("#myDiv");
divElement.classList.add("bar");
divElement.classList.add("foo");
divElement.classList.add("zorb");
divElement.classList.add("baz");
console.log(divElement.classList);

let divElement = document.querySelector("#myDiv");
divElement.classList.remove("foo");
console.log(divElement.classList);

let divElement = document.querySelector("#myDiv");
divElement.classList.toggle("foo"); // удаляет foo
divElement.classList.toggle("foo"); // добавляет foo
divElement.classList.toggle("foo"); // удаляет foo
console.log(divElement.classList);

let divElement = document.querySelector("#myDiv");
if (divElement.classList.contains("bar") == true) {
// делает что-нибудь
}

# head 28 DOM navigation

let bodyElement = document.querySelector("body");
if (bodyElement.firstChild) {
// Делает что-нибудь интересное
}

let bodyElement = document.body;
for (let i = 0; i < bodyElement.children.length; i++) {
let childElement = bodyElement.children[i];
document.writeln(childElement.tagName);
}

function theDOMElementWalker(node) {
if (node.nodeType == Node.ELEMENT_NODE) {
console.log(node.tagName);
node = node.firstChild;
while (node) {
theDOMElementWalker(node);
node = node.nextSibling;
}
}
}

let texasRanger = document.querySelector("#texas");
theDOMElementWalker(texasRanger);

# head 29. create elements

## create

let myElement = document.createElement("p");

let newElement = document.createElement("p");
let bodyElement = document.querySelector("body");
let h1Element = document.querySelector("h1");
newElement.textContent = "I exist entirely in your imagination.";
bodyElement.insertBefore(newElement, h1Element.nextSibling);

## delete elems

let newElement = document.createElement("p");
let bodyElement = document.querySelector("body");
let h1Element = document.querySelector("h1");
newElement.textContent = "I exist entirely in your imagination.";
bodyElement.appendChild(newElement);
newElement.parentNode.removeChild(newElement);
newElement.remove();

## clone elems

let bodyElement = document.querySelector("body");
let item = document.querySelector("h1");
let clonedItem = item.cloneNode(false);
// добавление клонированного элемента в DOM
bodyElement.appendChild(clonedItem);

# head 30 browser dev tools

## view DOM
<!DOCTYPE html>
<html>
<head>
<title>Random Color Generator!</title>
<style>
h2 {
font-family: Arial, Helvetica;
font-size: 100px;
color: #FFF;
text-shadow: 0px 0px 11px #333333;
margin: 0;
padding: 30px;
}
</style>
<body style="background-color: rgb(75, 63, 101);">
<h2>Random
<br>Color
<br>Generator</h2>
<script src="js/randomColor.js"> </script>
<script>
let bodyElement = document.querySelector("body");
bodyElement.style.backgroundColor = getRandomColor();
</script>
</body>
</html>

## js debug

debugging in the browser allows you to repeat the page loading step by step. function by function, using special buttons for this.

## console

in the developer's console, we get access to all objects in the viewport, including the main window.

# head 31 event

source.addEventListener(eventName, eventHandler, false);

document.addEventListener("click", changeColor, false);
function changeColor(event) {
// I am important!!!
}

document.addEventListener("click", changeColor, false);
document.removeEventListener("click", changeColor, false);
function changeColor() {
document.body.style.backgroundColor = "#FFC926";
}

# 32. events. bubbling and capturing

<!DOCTYPE html>
<html>
<head>
<title>Events!</title>
</head>
<body id="theBody" class="item">
<div id="one_a" class="item">
<div id="two" class="item">
<div id="three_a" class="item">
<button id="buttonOne" class="item">one</button>
</div>
<div id="three_b" class="item">
<button id="buttonTwo" class="item">two</button>
<button id="buttonThree" class="item">three</button>
</div>
</div>
</div>
<div id="one_b" class="item">
</div>
<script>
</script>
</body>
</html>

item.addEventListener("click", doSomething, true);
item.addEventListener("click", doSomething, false);

function handleClick(e) {
e.stopPropagation();
// что-нибудь делает
}

function overrideScrollBehavior(e) {
e.preventDefault();
// делает что-нибудь
}

# head 33. mouseEvent

## click & dbclick
let button = document.querySelector("#myButton");
button.addEventListener("click", doSomething, false);
function doSomething(e) {
console.log("Mouse clicked on something!");
}

let button = document.querySelector("#myButton");
button.addEventListener("dblclick", doSomething, false);
function doSomething(e) {
console.log("Mouse clicked on something...twice!");
}


## over & out
let button = document.querySelector("#myButton");
button.addEventListener("mouseover", hovered, false);
button.addEventListener("mouseout", hoveredOut, false);
function hovered(e) {
console.log("Hovered!");
}
function hoveredOut(e) {
console.log("Hovered Away!");
}

## mousedown & mouseup
let button = document.querySelector("#myButton");
button.addEventListener("mousedown", mousePressed, false);
button.addEventListener("mouseup", mouseReleased, false);
button.addEventListener("click", mouseClicked, false);
function mousePressed(e) {
console.log("Mouse is down!");
}
function mouseReleased(e) {
console.log("Mouse is up!");
}
function mouseClicked(e) {
console.log("Mouse is clicked!");
}

## mousemove
let button = document.querySelector("#myButton");
button.addEventListener("mousemove", mouseIsMoving, false);
function mouseIsMoving(e) {
console.log("Mouse is on the run!");
}

## contextmenu
document.addEventListener("contextmenu", hideMenu, false);
function hideMenu(e) {
e.preventDefault();
}

## mouseEvent property
document.addEventListener("mousemove", mouseMoving, false);
function mouseMoving(e) {
console.log(e.screenX + " " + e.screenY);
}

let button = document.querySelector("#myButton");
document.addEventListener("mousemove", mouseMoving, false);
function mouseMoving(e) {
console.log(e.clientX + " " + e.clientY);
}

document.addEventListener("mousedown", buttonPress, false);
function buttonPress(e) {
if (e.button == 0) {
console.log("Left mouse button pressed!");
} else if (e.button == 1) {
console.log("Middle mouse button pressed!");
} else if (e.button == 2) {
console.log("Right mouse button pressed!");
} else {
console.log("Things be crazy up in here!!!");
}
}

## mouseWheel
function mouseWheeling(e) {
let scrollDirection;
let wheelData = e.wheelDelta;
if (wheelData) {
scrollDirection = wheelData;
} else {
scrollDirection = -1 * e.detail;
}
if (scrollDirection > 0) {
console.log("Scrolling up! " + scrollDirection);
} else {
console.log("Scrolling down! " + scrollDirection);
}
}

# head 34. KeyboardEvent

window.addEventListener("keydown", dealWithKeyboard, false);
window.addEventListener("keypress", dealWithKeyboard, false);
window.addEventListener("keyup", dealWithKeyboard, false);
function dealWithKeyboard(e) {
// вызывается, когда услышано любое из событий клавиатуры
}

window.addEventListener("keydown", checkKeyPressed, false);
function checkKeyPressed(e) {
if (e.keyCode == 65) {
console.log("The 'a' key is pressed.");
}
}

window.addEventListener("keypress", checkKeyPressed, false);
function checkKeyPressed(e) {
if (e.charCode == 97) {
console.log("The 'a' key is pressed.");
}
}

window.addEventListener("keydown", moveSomething, false);
function moveSomething(e) {
switch (e.keyCode) {
case 37:
// нажатие влево
break;
case 38:
// нажатие вверх
break;
case 39:
// нажатие вправо
break;
case 40:
// нажатие вниз
break;
}
}

window.addEventListener("keydown", keysPressed, false);
window.addEventListener("keyup", keysReleased, false);
let keys = [];
function keysPressed(e) {
// сохраняет запись о каждой нажатой клавише
keys[e.keyCode] = true;
// Ctrl + Shift + 5
if (keys[17] && keys[16] && keys[53]) {
// делает что-нибудь
}
// Ctrl + f
if (keys[17] && keys[70]) {
// делает что-нибудь
// предотвращает встроенное поведение браузера
e.preventDefault();
}
}
function keysReleased(e) {
// отмечает отпущенные клавиши
keys[e.keyCode] = false;
}