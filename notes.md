                                         **_Basic TypeScript Concepts_** 📘

 
**_Printing "Hello World" to the console_** 🖨️  ->
console.log('Hello world');


                                         **_Variables and Types_** 📝
😊 Def : Variables store data values with specified types.
Example: 'a' is a number storing the value 10
let a: number = 10;
console.log(a); // Output: 10

                                         **Basic Types:**
- **number:** Represents numeric values like integers and floats.
- **string:** Represents textual data.
- **boolean:** Represents logical values true or false.
- **null:** Represents a null value.
- **undefined:** Represents an undefined value.
- **void:** Represents the absence of any type.
- **any:** Represents any type, allowing values of any data type.
- **unknown:** Data types is unknown.

                                         **_Note_** 
😊 - **_ 'any' and 'unknown' types_🔍** ->
'any' allows variables to hold any value, while 'unknown' requires type checking.
Example1: 'b' can hold any value
let b: any = 10;
b = "String"; // Now 'b' holds a string value

Example2: 'c' initially holds a number, then a string after type checking
let c: unknown = 10;
c = "Prachi";
console.log(c); // Output: Prachi

                                         **_Arrays_** 📚
😊 Def: Arrays store multiple values of the same or different types.
Example1: Array with mixed types
let arr = [1, 2, "Prachi", true];

Example2: Array of numbers
let num: number[] = [1, 2, 3, 4];
num.forEach((n) => n.toString()); // Converting each number to string

Example3: Array of strings
let string: string[] = ["Prachi", "Paliwal"];
string.forEach((n) => n.toLowerCase()); // Converting each string to lowercase

                                         **_Constants and Arrays_** 🛑
😊 Def: Constants hold values that cannot be changed.
Example: 'numbers' is a constant array, but its elements can still be modified
const numbers = [1, 2, 3];
numbers.push(4);

                                         **_Tuples_** 📦
😊 Def: Tuples are arrays with fixed types and lengths.
Example1: Tuple with defined types and length
let foods: [number, string, number, string] = [1, "Papaya", 2, "Graphes"];

Example2: Array with union type
let foodss: (number | string)[] = [1, 2, 3, "Apple", "Mango", 4];

                                         **_Enum_** 🏷️
😊 Def: Enums organize related values.
Example1: Enum representing different shirt sizes
enum ShirtSize {
  Large = "Large",
  Medium = "Medium",
  XL = "Extra Large",
  XXL = "Super Large"
}

Example2: Assigning 'Medium' from ShirtSize enum
let size: ShirtSize = ShirtSize.Medium;
console.log(size); // Output: Medium

                                         **_Functions_** 🎵
😊 Def: Functions perform specific tasks.
Example1: Function accepting any type of argument
function myFun(text: any) {
  return "Hello world" + text;
}
myFun(12); // Calling function with number argument

Example2: Function accepting only numbers
function myFun1(text: number) {
  return "Hello world" + text;
}
myFun1(12); // Calling function with number argument

Example3: Function with specified parameter and return types
function myFun2(text: string): number {
  if (text == "Hello") {
    return 1;
  } else {
    return 0;
  }
}
myFun2("Hello"); // Calling function with string argument

                                         **_Objects_** 🧑‍🤝‍🧑
😊 Def: Objects have properties and methods.
Example1: Defining a type for a Friend object
type Friend = {
  name: string,
  age: number,
  college: string
}

Example2: Creating an object of type Friend
let friend: Friend = {
  name: "Prachi",
  age: 19,
  college: "Cdgi"
}
console.log(friend.college); // Accessing property of object

Example3: Defining a type for a Food object
type FoodType = {
  name: string,
  favorite(foodName: string): void;
}

Example4: Creating an object of type FoodType with a method
let foodType: FoodType = {
  name: "Apple",
  favorite(foodName: string) {
    console.log("Favorite food is", foodName);
  }
}
foodType.favorite("Mango"); // Calling the method with an argument

                                         **_Union Types_** 🔄
😊 Def:  In TypeScript, union types allow variables to hold values of multiple specified types.
let value: number | string; // Declaring a variable that can hold either a number or a string
value = 10; // Valid
value = "Hello"; // Also valid

                                         **_Intersection Types_** 📝
😊 Def: Intersection types combine multiple types into one.
type A = { a: number };
type B = { b: string };
let obj: A & B = { a: 1, b: "hello" }; // Creating an object that has properties from both types A and B

