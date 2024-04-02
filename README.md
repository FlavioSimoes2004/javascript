# JAVASCRIPT
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