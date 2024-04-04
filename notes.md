                                         **_Basic TypeScript Concepts_** 📘

 
**_Printing "Hello World" to the console_** 🖨️  <br>
console.log('Hello world');


                                         **_Variables and Types_** 📝
😊 Def : Variables store data values with specified types. <br>
Example: 'a' is a number storing the value 10 <br>
let a: number = 10; <br>
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
😊 - **_ 'any' and 'unknown' types_🔍**  <br>
'any' allows variables to hold any value, while 'unknown' requires type checking. <br>
Example1: 'b' can hold any value <br>
let b: any = 10; <br>
b = "String"; // Now 'b' holds a string value <br>

Example2: 'c' initially holds a number, then a string after type checking <br>
let c: unknown = 10; <br>
c = "Prachi"; <br>
console.log(c); // Output: Prachi <br>

                                         **_Arrays_** 📚
😊 Def: Arrays store multiple values of the same or different types. <br>
Example1: Array with mixed types <br>
let arr = [1, 2, "Prachi", true]; <br>

Example2: Array of numbers <br>
let num: number[] = [1, 2, 3, 4]; <br>
num.forEach((n) => n.toString()); // Converting each number to string <br>

Example3: Array of strings <br>
let string: string[] = ["Prachi", "Paliwal"]; <br>
string.forEach((n) => n.toLowerCase()); // Converting each string to lowercase <br>

                                         **_Constants and Arrays_** 🛑
😊 Def: Constants hold values that cannot be changed. <br>
Example: 'numbers' is a constant array, but its elements can still be modified <br>
const numbers = [1, 2, 3]; <br>
numbers.push(4); <br>

                                         **_Tuples_** 📦
😊 Def: Tuples are arrays with fixed types and lengths. <br>
Example1: Tuple with defined types and length <br>
let foods: [number, string, number, string] = [1, "Papaya", 2, "Graphes"]; <br>

Example2: Array with union type <br>
let foodss: (number | string)[] = [1, 2, 3, "Apple", "Mango", 4]; <br>

                                         **_Enum_** 🏷️
😊 Def: Enums organize related values. <br>
Example1: Enum representing different shirt sizes <br>
enum ShirtSize { <br>
  Large = "Large", <br>
  Medium = "Medium", <br>
  XL = "Extra Large", <br>
  XXL = "Super Large" <br>
} <br>

Example2: Assigning 'Medium' from ShirtSize enum <br>
let size: ShirtSize = ShirtSize.Medium; <br>
console.log(size); // Output: Medium <br>

                                         **_Functions_** 🎵
😊 Def: Functions perform specific tasks. <br>
Example1: Function accepting any type of argument <br>
function myFun(text: any) { <br>
  return "Hello world" + text; <br>
} 
myFun(12); // Calling function with number argument <br>

Example2: Function accepting only numbers <br>
function myFun1(text: number) { <br>
  return "Hello world" + text; <br>
} <br>
myFun1(12); // Calling function with number argument <br>

Example3: Function with specified parameter and return types <br>
function myFun2(text: string): number { <br>
  if (text == "Hello") { <br>
    return 1; <br>
  } else { <br>
    return 0; <br>
  } <br>
} <br>
myFun2("Hello"); // Calling function with string argument <br>

                                         **_Objects_** 🧑‍🤝‍🧑
😊 Def: Objects have properties and methods. <br>
Example1: Defining a type for a Friend object <br>
type Friend = { <br>
  name: string, <br>
  age: number, <br>
  college: string <br>
} <br>

Example2: Creating an object of type Friend <br>
let friend: Friend = { <br>
  name: "Prachi", <br>
  age: 19, <br>
  college: "Cdgi" <br>
} <br>
console.log(friend.college); // Accessing property of object <br>

Example3: Defining a type for a Food object <br>
type FoodType = { <br>
  name: string, <br>
  favorite(foodName: string): void; <br>
} <br>

Example4: Creating an object of type FoodType with a method <br>
let foodType: FoodType = { <br>
  name: "Apple", <br> 
  favorite(foodName: string) { <br>
    console.log("Favorite food is", foodName); <br>
  } <br>
} <br>
foodType.favorite("Mango"); // Calling the method with an argument <br>

                                         **_Union Types_** 🔄
😊 Def:  In TypeScript, union types allow variables to hold values of multiple specified types. <br>
let value: number | string; // Declaring a variable that can hold either a number or a string <br>
value = 10; // Valid <br>
value = "Hello"; // Also valid <br>

                                         **_Intersection Types_** 📝
😊 Def: Intersection types combine multiple types into one. <br>
type A = { a: number }; <br>
type B = { b: string }; <br>
let obj: A & B = { a: 1, b: "hello" }; // Creating an object that has properties from both types A and B <br>

