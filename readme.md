
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

let total = 4 + 26;
let average = total / 2;
let doublePi = 2*3.14159;
let subtractItem = 50 — 25;
let remainder = total % 7;
let more = (1 + average * 10) / 5;

let leet = 0o2471;
let leet = 0x539;

let myLoveForYou = Infinity * 2;

