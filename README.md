# OCaml_Quick_guide_and_Training
Fast getting started and cheat sheet for OCaml. Some exercices and problems with their solutions

## 1. Set-up

### 1.a. Installing OCaml
```shell
brew install ocaml
```
### 1.b. Installing the package manager
```shell
brew install opam
```

### 1.c. OCaml TopLevel vs UTop
When you run ```ocaml```, you enter the OCaml REPL, Read-Eval-Print-Loop. It is the TopLevel system.

UTop, the Universal TopLevel is an improved interface compare to the OCaml topLevel. You can install it using __opam__,
```shell
opam install utop
```

### 1.d. Beyond the standard library
OCaml comes with its own libraries, the minimal system needed to run OCaml programs.

- Base extends the OCaml standard library;

- Core-kernel extends Base;

- Core extends Core-kernel, notably with its Unix API.


**Nota Bene:** we drop the REPL stage, since we learn programming languages to be able to run scripts and programs in standalone units, not in an interactive shell.


### 1.e. OCaml type inference
Type inference is the ability of OCaml to determine the type of an expression. The type of an expression is inferred from the available type information about the components of that expression.






## 2. Building, Compiling, Running

### 2.a. Building


### 2.b. Compiling

### 2.c. Running

### 2.d. Running with command line arguments





## 3. OCaml cheat sheet

### OCaml conventions

• Varialbles

• functions


### let binding, recursive binding

### Funs (anonymous functions), functions

### Tuples, Lists

### Simple imperative features





## 4. Getting some help

Of course, OCaml's website is the primary source of information.



## 5. More about imperative OCaml
=> More than necessary



## 6. Object Oriented programming in OCaml
Why?

- One example of use :

- Followed by "How to make it functional"? > OO needless, right?





## R. Some references: books

• Real Worrld OCaml
