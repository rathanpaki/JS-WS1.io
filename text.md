// https://docs.google.com/document/d/1roNvmZYxcsp11m0bIuACM9IJNJif9Y0t5uxqZv2pclU/edit

// 1 Ques

function fullName(firstName, lastName) {
  return `${firstName} ${lastName}`;
}

// 2 Ques

console.log(
  "The quote 'There is no exercise better for the heart than reaching down and lifting people up.' by John Holmes teaches\n us to help one another."
);

// 3 Ques

console.log("11111\n21248\n313927\n4141664\n51525125");

// 4 ques

let sentence =
  "There is a commonly stated “rule” of grammar that beginning a sentence with and, or any other conjunction, is a mistake. But this is just not true. This supposed “rule” has no basis in actual writing, and even formal writing features plenty of sentences that start with and and other conjunctions. And we think that is really cool.";
let count = (sentence.match(/and/g) || []).length;
console.log(count);

// 5 Ques

let now = new Date();
console.log(`Year now: ${now.getFullYear()}`);
console.log(`Month now as a number: ${now.getMonth() + 1}`);
console.log(`Today: ${now.getDate()}`);
console.log(`Today as a number: ${now.getDay()}`);

// 6 Ques

let slope = 2;
let yIntercept = -2;
let xIntercept = -yIntercept / slope;

console.log(`Slope: ${slope}`);
console.log(`x-intercept: ${xIntercept}`);
console.log(`y-intercept: ${yIntercept}`);

// 7 Ques

let x1 = 2,
  y1 = 2,
  x2 = 6,
  y2 = 10;
let slopeBetweenPoints = (y2 - y1) / (x2 - x1);
console.log(
  `The slope between the points (2, 2) and (6, 10) is ${slopeBetweenPoints}`
);

// 8 Ques

let hours = prompt("Enter the working Hous:");
let ratePerHour = 20;
let weeklyEarning = hours * ratePerHour;
console.log(`Your weekly earning is ${weeklyEarning}`);

// 9 Ques

let birthYear = prompt("Enter birth year:");
let currentYear = new Date().getFullYear();
let age = currentYear - birthYear;

if (age >= 18) {
  console.log(`You are ${age}. You are old enough to drive.`);
} else {
  console.log(
    `You are ${age}. You will be allowed to drive after ${18 - age} years.`
  );
}

// 10 Ques

let numbers1 = [1, 2, 3, 4, 5, 6, 7];
let evenNumbers = numbers1.filter(function (number) {
  return number % 2 === 0;
});
console.log(evenNumbers);

// 11 Ques

let numbers2 = [1, 2, 3, 4, 5];
// let squaredNumbers = numbers2.map(function (number) {
//   return number * number;
// });

// using arrowfunction
let squaredNumbers = numbers2.map((number) => {
  return number * number;
});
console.log(squaredNumbers);

// 13 Ques

const greets = (name) => {
  return `Welcome ${name} to the team.`;
};

console.log(greets("Ran"));
console.log(greets("Sara"));

// 12 Ques

const books = [
  {
    title: "To Kill a Mockingbird",
    author: "Harper Lee",
    genre: "Fiction",
    pages: 336,
    publication_year: 1925,
  },
  {
    title: "1984",
    author: "George Orwell",
    genre: "Dystopian",
    pages: 328,
    publication_year: 1949,
  },
  {
    title: "Pride and Prejudice",
    author: "Jane Austen",
    genre: "Romance",
    pages: 432,
    publication_year: 1813,
  },
  {
    title: "The Great Gatsby",
    author: "F. Scott Fitzgerald",
    genre: "Classic",
    pages: 180,
    publication_year: 1925,
  },
];

// 1. MAP:
// Get an array of all titles:

const titles = books.map((book) => book.title);
console.log(titles);

// Get an array of all authors:

const authors = books.map((book) => book.author);
console.log(authors);

// Get an array of objects with just title and author properties:

const titlesAndAuthors = books.map((book) => ({
  title: book.title,
  author: book.author,
}));
console.log(titlesAndAuthors);

// 2. REDUCE:
// Get the total number of pages for all books:

const totalPages = books.reduce((total, book) => total + book.pages, 0);
console.log(totalPages);

// recommend methode
const totalNumber = books.reduce((sum, books) => {
  return sum + parseInt(books.pages);
}, 0);
console.log("Total Number of pages is " + totalNumber);

// Get the total number of books by publication_year (using a map of publication_year to count):

const booksByYear = books.reduce((acc, book) => {
  acc[book.publication_year] = (acc[book.publication_year] || 0) + 1;
  return acc;
}, {});
console.log(booksByYear);

// recoment methode
const totalNumberOfPublicationYear = books.reduce((result, books) => {
  if (typeof result[books.publication_year] === "undefined") {
    result[books.publication_year] = 1;
  } else {
    result[books.publication_year] += 1;
  }
  return result;
}, {});
console.log(totalNumberOfPublicationYear);

// Get the total number of characters in all the book titles:

const totalTitleCharacters = books.reduce(
  (total, book) => total + book.title.length,
  0
);
console.log(totalTitleCharacters);

// Get the total number of books by genre (using a map of genre to count):

const booksByGenre = books.reduce((acc, book) => {
  acc[book.genre] = (acc[book.genre] || 0) + 1;
  return acc;
}, {});
console.log(booksByGenre);

// 3. FILTER:
// Filter books with more than 100 pages:

//one methode
// const filterBooksByPage = books.filter((books) => {
//   return books.pages > 100;
// });
// console.log(filterBooksByPage);

// second methode
const booksMoreThan100Pages = books.filter((book) => book.pages > 100);
console.log(booksMoreThan100Pages);

// Filter books with less than 200 pages:

const booksLessThan200Pages = books.filter((book) => book.pages < 200);
console.log(booksLessThan200Pages);

// Filter books with a genre of "Fiction":

const fictionBooks = books.filter((book) => book.genre === "Fiction");
console.log(fictionBooks);

// Filter books with a genre of "Romance":

const romanceBooks = books.filter((book) => book.genre === "Romance");
console.log(romanceBooks);

// 14 Ques

const litres = (time) => Math.floor(time * 0.5);

console.log(litres(0));
console.log(litres(2));
console.log(litres(1.4));

// 15 Ques

const positiveSum = (arr) => {
  return arr.filter((num) => num > 0).reduce((sum, num) => sum + num, 0);
};

console.log(positiveSum([1, 2, 3, 4, 5]));
console.log(positiveSum([1, -2, 3, 4, 5]));
console.log(positiveSum([-1, 2, 3, 4, -5]));
console.log(positiveSum([-1, -2, -3, -4, -5]));
console.log(positiveSum([]));

// // 16 Ques

const calculateBMI = (weight, height) => {
  const bmi = weight / (height * height);

  if (bmi < 18.5) {
    return `Underweight: BMI is ${bmi.toFixed(2)}`;
  } else if (bmi >= 18.5 && bmi <= 24.9) {
    return `Normal weight: BMI is ${bmi.toFixed(2)}`;
  } else if (bmi >= 25 && bmi <= 29.9) {
    return `Overweight: BMI is ${bmi.toFixed(2)}`;
  } else {
    return `Obese: BMI is ${bmi.toFixed(2)}`;
  }
};

console.log(calculateBMI(70, 1.75));
console.log(calculateBMI(50, 1.6));
console.log(calculateBMI(90, 1.8));
console.log(calculateBMI(110, 1.75));

// //part 2

// Q2

let a = 1;
a > 0 ? console.log("a is positive") : console.log("a is not positive");

// Q2

let number = parseInt(prompt("Enter a number:"));
console.log(`The number ${number} is ${number % 2 === 0 ? "Even" : "Odd"}.`);

// Q3

function findGreater(num1, num2) {
  return num1 > num2 ? num1 : num2;
}
console.log(findGreater(10, 20));
console.log(findGreater(50, 30));

// Q4

function getTicketPrice(age) {
  return age < 12 ? 5 : age < 18 ? 10 : age < 60 ? 20 : 15;
}
console.log(getTicketPrice(5));
console.log(getTicketPrice(15));
console.log(getTicketPrice(30));
console.log(getTicketPrice(65));

//Q5

function isLeapYear(year) {
  return (year % 4 === 0 && year % 100 !== 0) || year % 400 === 0;
}
console.log(isLeapYear(2020));
console.log(isLeapYear(2021));

// Q6

function getDiscount(price) {
  return price >= 100 ? 20 : price >= 50 ? 10 : 0;
}
console.log(getDiscount(120));
console.log(getDiscount(75));
console.log(getDiscount(30));

// Q7

function greetUser(hour) {
  return hour < 12
    ? "Good Morning"
    : hour < 18
    ? "Good Afternoon"
    : "Good Evening";
}
const currentHour = new Date().getHours();
console.log(greetUser(currentHour));

// Q8

function numberGuessingGame(secretNumber, guess) {
  return guess === secretNumber
    ? "Correct"
    : guess > secretNumber
    ? "Lower"
    : "Higher";
}
const secretNumber = 7;
console.log(numberGuessingGame(secretNumber, 5));
console.log(numberGuessingGame(secretNumber, 10));
console.log(numberGuessingGame(secretNumber, 7));

// Part 3

// Q1

for (let i = 0; i <= 5; i++) {
  console.log(i);
}

// Q2

let sum = 0;
for (let i = 0; i < 100; i++) {
  sum += i;
}
console.log(sum);

// Q3

let sumEven = 0;
for (let i = 10; i <= 100; i += 2) {
  sumEven += i;
}
console.log(sumEven);

// Q4

let arr = [43, "what", 9, true, "cannot", false, "be", 3, true];
for (let i = arr.length - 1; i >= 0; i--) {
  console.log(arr[i]);
}

// Q5

let arr_3 = [4, 6, 7];
let arr_4 = [8, 1, 9];
let sumArray = [];

for (let i = 0; i < arr_3.length; i++) {
  sumArray.push(arr_3[i] + arr_4[i]);
}
console.log(sumArray);

// Q6

let str1 = "javascript";
let resultStr = "";

for (let i = 0; i < str1.length; i++) {
  resultStr += (i + 1) % 2 === 0 ? "Z" : str1[i];
}
console.log(resultStr);

// Q7

let arr_1 = [3, 5, 22, 5, 7, 2, 45, 75, 89, 21, 2];
let arr_2 = [9, 2, 42, 55, 71, 22, 4, 5, 90, 25, 26];

let totalSum = 0;

for (let i = 0; i < arr_1.length; i++) {
  totalSum += arr_1[i] + arr_2[i];
}
console.log(totalSum);
