# JAVASCRIPT
Para executar um arquivo .js, precisa do Node.js e executar o comando: node fileName.js
## PRINT
<pre>
console.log("Hello World");
</pre>

## COMMENT
<pre>
//Prints 5 to the console
console.log(5);
</pre>
OU
<pre>
console.log(5);  // Prints 5 
</pre>
OU
<pre>
/*
    comment
*/
</pre>
OU
<pre>
console.log(/*IGNORED!*/ 5);  // Still just prints 5 
</pre>

## STRING
#### CONCATENAR(JUNTAR)
<pre>
console.log('front ' + 'space'); 
// Prints 'front space'
console.log('back' + ' space'); 
// Prints 'back space'
console.log('no' + 'space'); 
// Prints 'nospace'
console.log('middle' + ' ' + 'space'); 
// Prints 'middle space'
</pre>

#### INTERPOLATION
<pre>
const myPet = 'armadillo';
console.log(`I own a pet ${myPet}.`);
// Output: I own a pet armadillo.
</pre>
Tem que começar com ser com ' e não com ".

#### TAMANHO
<pre>
console.log('Hello'.length); // Prints 5
</pre>

#### MÉTODOS
<pre>
console.log('hello'.toUpperCase()); // Prints 'HELLO'
console.log('Hey'.startsWith('H')); // Prints true
console.log('    Remove whitespace   '.trim()); //Remove white spaces that are useless
</pre>

## BUILT-IN OBJECTS
<pre>
console.log(Math.random()); // Prints a random number between 0 and 1
</pre>

Para gerar um número entre 0 e x, basta fazer o seguinte:
<pre>
Math.random() * x;
</pre>
Vai gerar um <strong>DECIMAL</strong> entre 0 e 50. Para resolver isso, basta fazer:
<pre>
Math.floor(Math.random() * 50);
</pre>
o 'Math.floor()' pega um número decimal e arredonda ele para o inteiro <strong>MENOR</strong> mais próximo.\
Já o 'Math.ceil()' pega um número decimal e arredonda ele para o inteiro <strong>MAIOR</strong> mais próximo.\
\
OUTRAS FUNÇÕES:
<pre>
console.log(Number.isInteger(2017));
</pre>

## VARIABLES
Em 2015, houve uma atualização no javascript, onde acrescentou mais 2 keywords, o 'let' e 'const', para criar ou declarar variáveis. Antes disso,
os programadores apenas podiam usar a keyword 'var' para declarar variáveis.
<pre>
var myName = 'Arya';
console.log(myName);
</pre>

### let
a keyword 'let' indica que aquela variável pode ter seu valor alterado.
<pre>
let meal = 'Enchiladas';
console.log(meal); // Output: Enchiladas
meal = 'Burrito';
console.log(meal); // Output: Burrito
</pre>

### const
É uma constante, uma variável que seu valor não pode ser alterado de forma alguma.
<pre>
const myName = 'Gilberto';
console.log(myName); // Output: Gilberto
</pre>

### typeof operator
<pre>
const unknown1 = 'foo';
console.log(typeof unknown1); // Output: string

const unknown2 = 10;
console.log(typeof unknown2); // Output: number

const unknown3 = true; 
console.log(typeof unknown3); // Output: boolean
</pre>

## IS EQUAL OPERATOR
Diferente de muitas linguagens, onde para comparar se uma variável é igual ou não usa o '==', no javascript usa-se '==='. O diferente do javascript é '!=='.

## TRUTHY AND FALSY ASSIGNMENT
### VARIABLE
<pre>
let myVariable = 'I Exist!';

if (myVariable) {
   console.log(myVariable)
} else {
   console.log('The variable does not exist.')
}
</pre>
Para entrar nesse else, a variável tem que ter esses valores:
- igual a 0
- Strings vazia como: '' ou ""
- igual a null
- igual a undefined
- NaN, not a number

### SHORT-CIRCUIT EVALUATION
<pre>
let username = '';
let defaultName;

if (username) {
  defaultName = username;
} else {
  defaultName = 'Stranger';
}

console.log(defaultName); // Prints: Stranger
</pre>
\
OU
<pre>
let username = '';
let defaultName = username || 'Stranger';

console.log(defaultName); // Prints: Stranger
</pre>

## TERNARY OPERATOR
DISSO
<pre>
let isNightTime = true;

if (isNightTime) {
  console.log('Turn on the lights!');
} else {
  console.log('Turn off the lights!');
}
</pre>
\
PRA ISSO
<pre>
isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
</pre>

## FUNCTIONS
### FUNCTION DECLARATION
A declaração de uma função consiste em:
- a keyword 'function'
- nome da função seguido de parenteses
- e o corpo da função, que são os colchetes '{}'
<!-- END OF LIST -->
Exemplo:
<pre>
greetWorld(); // Output: Hello, World!

function greetWorld() {
  console.log('Hello, World!');
}
</pre>

OU (FUNCTION EXPRESSION)

<pre>
const plantNeedsWater = function(day){
  if(day === 'Wednesday')
  {
    return true;
  }
  else
  {
    return false;
  }
}
</pre>

OU (ARROW FUNCTION)

<pre>
const plantNeedsWater = (day) => {
  if (day === 'Wednesday') {
    return true;
  } else {
    return false;
  }
};
</pre>

OU (CONCISE BODY ARROW FUNCTION)

<pre>
const plantNeedsWater = day => day === 'Wednesday' ? true : false;
</pre>

### PARAMETERS
<pre>
function sayThanks(name) {
  console.log('Thank you for your purchase '+ name + '! We appreciate your business.');
}

sayThanks('Cole');
</pre>

#### DEFAULT PARAMETERS
<pre>
function makeShoppingList(item1='milk', item2='bread', item3='eggs'){
  console.log(`Remember to buy ${item1}`);
  console.log(`Remember to buy ${item2}`);
  console.log(`Remember to buy ${item3}`);
}
</pre>

### RETURN
<pre>
function monitorCount(rows, columns){
  return rows * columns;
}
</pre>

### FUNCTION AS DATA
<pre>
const checkThatTwoPlusTwoEqualsFourAMillionTimes = () => {
  for(let i = 1; i <= 1000000; i++) {
    if ( (2 + 2) != 4) {
      console.log('Something has gone very wrong :( ');
    }
  }
};

// Write your code below
const isTwoPlusTwo = checkThatTwoPlusTwoEqualsFourAMillionTimes
isTwoPlusTwo()
console.log(isTwoPlusTwo.name) //prints 'checkThatTwoPlusTwoEqualsFourAMillionTimes'
</pre>

### FUNCTIONS AS PARAMETERS
<pre>
const addTwo = num => {
  return num + 2;
}

const checkConsistentOutput = (func, val) => {
  let checkA = val + 2;
  let checkB = func(val);
  return checkA === checkB ? func(val) : 'inconsistent results';  
}

console.log(checkConsistentOutput(addTwo, 10));
</pre>

## ARRAYS
<pre>
let newYearsResolutions = ['Keep a journal', 'Take a falconry class', 'Learn to juggle'];
</pre>
String também são arrays no javascript

### PRINT
Podemos printar um array fazendo:
<pre>
console.log(array);
</pre>

### REASSIGN ARRAY
<pre>
let array = [1, 2, 3];
array = [4, 5, 6];
console.log(array);
</pre>

### TAMANHO
<pre>
console.log(array.length);
</pre>

### .PUSH METHOD
<pre>
const itemTracker = ['item 0', 'item 1', 'item 2'];

itemTracker.push('item 3', 'item 4');

console.log(itemTracker); 
// Output: ['item 0', 'item 1', 'item 2', 'item 3', 'item 4'];
</pre>

### .POP METHOD
<pre>
const newItemTracker = ['item 0', 'item 1', 'item 2'];

const removed = newItemTracker.pop();

console.log(newItemTracker); 
// Output: [ 'item 0', 'item 1' ]
console.log(removed);
// Output: item 2
</pre>

### MORE METHODS
#### .JOIN
<pre>
const gameObjects = ['rock', 'paper', 'scissors'];
const joinNoSeparator = gameObjects.join();
const joinWithSeparator = gameObjects.join(' + ');

console.log('No separator: ', joinNoSeparator);
console.log('With separator: ', joinWithSeparator);
/*OUTPUT:
No separator:  rock,paper,scissors
With separator:  rock + paper + scissors*/
</pre>

#### .SHIFT
Remove o primeiro elemento de um array
<pre>
const groceryList = ['orange juice', 'bananas', 'coffee beans', 'brown rice', 'pasta', 'coconut oil', 'plantains'];

groceryList.shift() //remove the first item from the array
console.log(groceryList)
</pre>

#### .UNSHIFT
Adiciona um elemento no início do array.
<pre>
groceryList.unshift('popcorn')
console.log(groceryList)
</pre>

#### INDEXOF
<pre>
const pastaIndex = groceryList.indexOf('pasta');
</pre>

## ARRAYS AND FUNCTIONS
<pre>
const flowers = ['peony', 'daffodil', 'marigold'];

function addFlower(arr) {
  arr.push('lily');
}

addFlower(flowers);

console.log(flowers); // Output: ['peony', 'daffodil', 'marigold', 'lily']
</pre>

## MATRIX
<pre>
numberClusters = [[1, 2], [3, 4], [5, 6]]
const target = numberClusters[2][1]
</pre>

## LOOPS
### FOR
<pre>
for (let counter = 0; counter < 4; counter++) {
  console.log(counter);
}
</pre>

### WHILE
<pre>
// A while loop that prints 1, 2, and 3
let counterTwo = 1;
while (counterTwo < 4) {
  console.log(counterTwo);
  counterTwo++;
}
</pre>

### DO...WHILE
<pre>
let countString = '';
let i = 0;

do {
  countString = countString + i;
  i++;
} while (i < 5);

console.log(countString);
</pre>

## ITERATORS
### .FOREACH
Vai executar o mesmo código para cada elemento do array.
<pre>
const fruits = ['mango', 'papaya', 'pineapple', 'apple'];

// Iterate over fruits below
function print(item){
  console.log('I want to eat a ' + item)
}

fruits.forEach(print)
</pre>

### .MAP
retorna um novo array com as modificações feitas no corpo.
<pre>
const animals = ['Hen', 'elephant', 'llama', 'leopard', 'ostrich', 'Whale', 'octopus', 'rabbit', 'lion', 'dog'];

// Create the secretMessage array below
const secretMessage = animals.map(string => {
  return string[0]
})

console.log(secretMessage.join('')); //prints HelloWorld
</pre>

### .FILTER
Retorna um array com os elementos filtrados.
<pre>
const words = ['chair', 'music', 'pillow', 'brick', 'pen', 'door']; 

const shortWords = words.filter(word => {
  return word.length < 6;
});
// shortWords only have elements with less than six letters
</pre>

### .FINDINDEX
Retorna apenas <strong>um</strong> index daquele elemento que for checado verdadeiro.
<pre>
const jumbledNums = [123, 25, 78, 5, 9]; 

const lessThanTen = jumbledNums.findIndex(num => {
  return num < 10;
});
</pre>

### .REDUCE
<pre>
const numbers = [1, 2, 4, 10];

const summedNums = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue
})

console.log(summedNums) // Output: 17
</pre>
\
OU
<pre>
const newNumbers = [1, 3, 5, 7];

const newSum = newNumbers.reduce((accumulator, currentValue) => {
  console.log('The value of accumulator: ', accumulator);
  console.log('The value of currentValue: ', currentValue);
  return accumulator + currentValue
}, 10) //this number 10 is the start value of accumulator

console.log(newSum)
</pre>

## OBJECTS
```javascript
const ship = {
  numCrew: 10,
  'The Ship Captain': 'I DONT KNOW'
};
```

### ACESSAR ATRIBUTOS
```javascript
let spaceship = {
  homePlanet: 'Earth',
  color: 'silver'
};
spaceship.homePlanet; // Returns 'Earth',
spaceship.color; // Returns 'silver',
```
\
OU
```javascript
let spaceship = {
  'Fuel Type' : 'Turbo Fuel',
  'Active Mission' : true,
  homePlanet : 'Earth', 
  numCrew: 5
 };

let isActive = spaceship['Active Mission']
console.log(spaceship['Active Mission'])
```

### ADICIONAR PROPRIEDADE
```javascript
let spaceship = {
  'Fuel Type' : 'Turbo Fuel',
  homePlanet : 'Earth',
  color: 'silver',
  'Secret Mission' : 'Discover life outside of Earth.'
};

spaceship.color = 'glorious gold'
spaceship.numEngines = 7 //Added property numEngines
```

### DELETAR PROPRIEDADE
```javascript
const spaceship = {
  'Fuel Type': 'Turbo Fuel',
  homePlanet: 'Earth',
  mission: 'Explore the universe' 
};
 
delete spaceship.mission;  // Removes the mission property
```

### METHODS
```javascript
const alienShip = {
  invade: function () { 
    console.log('Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.')
  }
};
```
\
OU
```javascript
const seila = {
    opa(){
        console.log("Joao is gay")
    }
};

seila.opa()
```

### OBJECTS INSIDE OBJECT
```javascript
const spaceship = {
     telescope: {
        yearBuilt: 2018,
        model: '91031-XLT',
        focalLength: 2032 
     },
    crew: {
        captain: { 
            name: 'Sandra', 
            degree: 'Computer Engineering', 
            encourageTeam() { console.log('We got this!') },
            'favorite foods': ['cookies', 'cakes', 'candy', 'spinach'] }
         }
    },
    engine: {
        model: 'Nimbus2000'
     },
     nanoelectronics: {
         computer: {
            terabytes: 100,
            monitors: 'HD'
         },
        'back-up': {
           battery: 'Lithium',
           terabytes: 50
         }
    }
};
```

#### ACESSING OBJECTS INSIDE OBJECT
```javascript
spaceship.nanoelectronics['back-up'].battery; // Returns 'Lithium'
const capFave = spaceship.crew.captain['favorite foods'][0]
```