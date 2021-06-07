# Writing My Own Programming Language


<!-- Write about why I'm doing this-->


## A brief overview on compilers

Compilers are translators, they translate code written in one language 
(normally a high-level language) into another language (normally a low level language).

The process of translating one language to another is divided into the following steps:

- Lexical analysis (scanning, tokenization).
- Syntax analaysis (parsing).
- Semantic analysis.
- intermediate code representation.
- code optimization.
- code generation. 

We can separate this steps into 3 different phases:

- Front end
- Middle end
- Back end

The *Front end* 

We start the front end by performing the *lexical analysis* on the source language,
it scans the input code and breaks it down into very tiny pieces called *lexemes* 
and assign each one to its  respective token, a token is nothing more than a 
"syntactic" category for the lexemes, they contain the token name (the lexeme category) 
and it's value. Just like words can be identified as "verbs" or "nouns", 
lexemes are assigned to tokens so that the compiler can know what each lexeme is. 

The next stage is the *Syntax Analysis*, here we check if the sequecence 
of tokens defined in the first stage form correct expressions. We do that by 
building an abstract syntax tree (AST), which builds a tree-like structure with 
our sequecence of tokens according to the rules of the grammar definied by the language.
If the programm is syntactically incorrent we can identify the error at this stage
of the compiler.

The last stage of the front end is the *Sematic analysis*, here we add semantic
information to our abstract syntax tree and build the symbol table, an important
data structure that is used as a lookup table by our compiler. At this step we
can perform type checking, object binding, definite assignment, and issue errors
if the semantic of the program is incorrect.   

The *Middle end*
