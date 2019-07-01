## Scope & Closures

1. Compiler theory
- Tokenizing/Lexing
- Parsing
- Code-Generation

2. Cheating lexicat
- eval
- with

3. IIFE - immediately invoked function expression

4. let
- implicitly hijacks any block's scope for its variable declaration
- declarations made with let will not hoist to the entire scope of the block they appear in
- the varialbe will be declared not just once for the loop, *but each iteration*

Notes:
- It doesn't matter where in the scope a declaration appears, the variable or functions 
belongs to the containing scope bubble, regardless.
- when you see `var a = 2` you probably think of that as one statement. But Javascript actually
thinks of it as two statements: `var a;` and `a = 2`. The first statement, the declaration, is processed
during the compilation phase. The second statement, the assignment, is left in place for the execution phase.
- function declaration are hoisted, function expression not. 
- function declaration are hoisted _before_ normal variables

5. Closure is when a function is able to remember and access its lexical scope even when
that function is executing outside its lexical scope.


```
btn.addEventListener('click', function () {
  ...
}, /*capturingPhase=*/false)
```