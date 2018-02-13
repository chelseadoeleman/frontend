# What is scope?
Where do variables live? Where are they saved?
How do these scope rules get set?
Engine en Compiler talk with the Scope.
Compiler: Tokens
Engine:

Scope word bepaald door functies of door blocks.
function a(){
  var b = 'b';
}
b kan alleen gebruikt worden in function a.
**Function scope** = Lexical Scope: Opbreken van code in kleine chunks (tokens)

function foo () {
  var b = 'b'; //var b niet bereikbaar buiten de functie foo.
}
console.log(b);
{
  var d = 'd'; //var luistert niet naar blocks. Leeft in een scope buiten het block.
  let c = 'c';
}
window - globale object terug
functie is Window - werkt onderwater.

## Compiler theory
 1. **Tokenizing/Lexing**: Breaking up a string of characters into meaningfull language. Whitespace may or may not persisted as a token, depends on wether it's meaningfull or not. Difference between Tokenizing and Lexing if tokens are identified in stateless or stateful way.
 2. **Parsing**: Taking an stream (array) turning it into a tree of nested elements. **AST**
 3. **Code-Generation**:

Javascript - Compiler first, than run right away.


## Understanding scope
Who is having the conversation

#### The cast
 1. Engine
 2. Compiler
 3. Scope

#### Back & Forth
An compiler will instead proceed as:
  1. Encountering: Compiler asks scope tot see if variable _a_ already exists on that scope collection. When it's **not** the case it asks to make var a
  2. Compiler then produce code for engine to later execute.

#### Compiler speak
**Assignment operation**
Left/right-hand side of an assignment (LHS and RHS).
LHS: Waar is de declaratie van de variable (containment).
RHS: Wat is de waarde van de variable.

#### Engine/Scope Conversation

## Nested scope
_RHS reference_

#### Building on Metaphors
_LHS and RHS reference_

## Errors
**Global Scope**
* ReferenceError is Scope resolution-failure related. Wanneer er geen referentie gevonden kan worden naar een variabele.
* TypeError: Scope resolution was succesful.

## Review (TL;DR)
