# 51 grupės klausimai

## Kodėl meta error (name.includes is not a function) jeigu loop nera us if?
```js
function hello(name) {

    if (name === undefined)  {
        return 'Error: No input found'
    }
    if (name === '')  {
        return 'Error: No input found'
    }

    let end = name.length;
    let endOne = name.length - 1;
    let endTwo = name.length - 2;


    if (typeof name === 'string') {                 // why do you need an if? (my brain too small)
        for (let i = 0; i < 10; i++) {              // loops trough 10 numbers
           if (name.includes(`${i}`)) {             // checks if any of the 10 numbers are in the string
            return 'ERROR: Input cannot contains numbers'
           }
        }
    }
    
    if (typeof name !== 'string') {
    return 'ERROR: Input must be a string'
    } 

    if (name.slice(endTwo, end) === 'as') {
        name = name.slice(0, endTwo);
        name += 'ai'
        return `Labas, ${name}!`;
    }
    if (name.slice(endTwo, end) === 'is') {
        name = name.slice(0, endTwo);
        name += 'i'
        return  `Labas, ${name}!`;
    }
    if (name.slice(endTwo, end) === 'us') {
        name = name.slice(0, endTwo);
        name += 'au'
        return  `Labas, ${name}!`;
    }
    if (name.slice(endOne, end) === 'ė') {
        name = name.slice(0, endOne);
        name += 'e';
        return  `Labas, ${name}!`;
    }  
    if (name.slice(endOne, end) === 'i' || 'y' || 'a') {
        return  `Labas, ${name}!`;
    }
    return `ERROR: Incorrect input`;
}

console.log(hello('Jonas'));
console.log(hello('Gedutis'));
console.log(hello('Ivijus'));
console.log(hello('Petrus'));
console.log(hello('Indrė'));
console.log(hello('Marija'));
console.log(hello('Žavi'));
console.log(hello('Sherry'));
console.log(hello('M4rji4'));
console.log(hello(123));
console.log(hello());



/* 
console.clear();
let name = 'Justinas';
console.log(name.slice(name.length - 2, name.length));

let badword = 'as3d';
let badword2 = 'asd';

function catcher(wr) {
    for (let i = 0; i < 10; i++) {
        if (wr.includes(`${i}`)) {
            return 'yes'
        }
    }
    return 'no';
}
  console.log(catcher(badword));
  console.log(catcher(badword2)); 
*/
    
```
