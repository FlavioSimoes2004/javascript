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