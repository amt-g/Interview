# Add two array value 

var a = [2, 3, 5, 6, 7];
var b = [1, 4, 0, 4];
function sumArray() {
  var c = [];
  for (var i = 0; i < Math.max(a.length, b.length); i++) {
    c.push((a[i] || 0) + (b[i] || 0));
  }
  console.log(c);
}
sumArray();

-------------------------------------

# Reverse word of string

function reverseWords(str) {
  let reverseWordArr = str
    .split(" ")                                           //  ["Hello", "Sir"]
    .map((word) => word.split("").reverse().join(""));
  console.log(reverseWordArr.join(" "));                  // olleH riS
}
reverseWords("Hello Sir");


# Reverse array without using reverse() method:

function reverseArray(arr) {
  let newArr = [];
  for (let i = arr.length - 1; i >= 0; i--) {
    newArr.push(arr[i]);
  }
  console.log(newArr);
}
reverseArray(["a", "b", "c", "d", "e", "f"]);


# output

function f(x, ...y) {
  return x * y.length;
}

console.log(f(3, "hello", true));     //6

function f(x, y, z) {
  return x + y + z;
}
const arr = [1, 2, 3];

console.log(f(...arr));

---

console.log(1 < 2 < 3);     // true
console.log(3 > 2 > 1);     // false

---------------------------------------

# Program to print product of even indexed elements in an Array

const arr = [1, 2, 1, 2, 3, 4, 1];
let output = arr.reduce((acc, curr) => {                             
  if (curr % 2 === 0) {
    acc *= curr;
  }
  return acc;
}, 1);
console.log(output);

## JavaScript program to find the most frequent element in an array

function mostFrequent(arr, len) {
  let maxcount = 0;
  let most_frequent_element;
  for (let i = 0; i < len; i++) {
    let count = 0;
    for (let j = 0; j < len; j++) {
      if (arr[i] === arr[j]) {
        count++;
      }
    }
    if (count > maxcount) {
      maxcount = count;
      most_frequent_element = arr[i];
    }
  }
  return { most_frequent_element, maxcount };
}
const arr = [30, 50, 50, 30, 30, 40];
let len = arr.length;
console.log(mostFrequent(arr, len));

## Filter with array of object

const arr = [
  { id: 1, name: "Amit", age: 18, role: "Design" },
  { id: 2, name: "", age: 16, role: "writer" },
  { id: 3, name: "chintu", age: 20, role: "developer" }
];

const newArr = arr.filter(emptyName);
console.log(newArr[0]);

function emptyName(el) {
  if (el.name === "") {
    return el;
  }
}

## find Min or Max number from array

const arr = [22,15,51,42,34,15,32,01,30,52,16,61];

console.log(Math.max.apply(null, arr))


## Write the code to find the vowels in string

const findVowels = str => {
  let count = 0
  const vowels = ['a', 'e', 'i', 'o', 'u']
  for(let char of str.toLowerCase()) {
    if(vowels.includes(char)) {
      count++
    }
  }
  return count
}
console.log(findVowels("Amit"));
