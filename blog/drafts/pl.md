# Writing My Own Programming Language


<!-- Write about why I'm doing this-->


## A brief overview on the compiler

The [Compiler][1] is a source-to-source compiler written in C, 
it translates the flow code into assembly language.

The process that the compiler uses to translate the flow language into assembly
is divided into the following steps:

- Lexical analysis (scanning and tokenization).
- Syntax analaysis (parsing).
- Semantic analysis (meaning).
- code generation (assembly). 

We can separate this steps into 2 different phases:

- **Front End**
- **Back End**

### The Front End 

We start on the front end performing the [**lexical analysis**][2], the compiler 
scans the input code and breaks it down into very tiny pieces called **lexemes** 
and assign each one to its respective token, in the compiler the tokens are 
structures that contain the token name(int) and it's value (when a int). 

The next stage is the [**Syntax Analysis**][3], here recognise the syntax and 
the structural elements of the input and ensure that they conform to the grammar
of the language. Our syntax analysis is made by a **recursive descent parser**,
we read in a token, and then look ahead the next token and based on what the 
next token is, we can decide what path we will take to parse the input. If the 
programm is syntactically incorrent we can identify the error at this stage of 
the compiler.

The last stage of the front end is the [**Sematic analysis**][4], which is where
the compiler understands the meaning of the input. We do that by building an 
**abstract syntax tree**(AST), where each recognised token is stored and enable us
to later on go trough it recursively to get the final value of the expression.
To deal with the problem of operator precedence we use a [Pratt Parser][5], it
has a table of precedence values associated with each token. 


### The Back End





References:

[1]: <https://en.wikipedia.org/wiki/Compiler> "Compilers"
[2]: <https://en.wikipedia.org/wiki/Lexical_analysis> "Lexical analysis"
[3]: <https://en.wikipedia.org/wiki/Parsing> "Syntax analysis" 
[4]: <https://en.wikipedia.org/wiki/Semantic_analysis_(compilers)> "Semantic analysis"
[5]: <https://en.wikipedia.org/wiki/Operator-precedence_parser#Pratt_parsing> "Pratt Parsing" 
[6]: <https://en.wikipedia.org/wiki/Code_generation_(compiler)> "Code generation" 
