# OCaml_Quick_guide_and_Training
Fast getting started and cheat sheet for OCaml. Some exercices and problems with their solutions

## 1. The OCaml REPL

Installing OCaml, then, the package manager and finally running the OCaml REPL, Read-Eval-Print-Loop :
```shell
$ brew install ocaml
$ brew install opam
$ ocaml
#       (* This is the OCaml REPL prompt *)
# #quit;;
```

### 1.1. OCaml TopLevel vs UTop

When running ```ocaml```, you enter the OCaml TopLevel system, a very minimalistic REPL. But you can get UTop, the Universal TopLevel, which is an improved interface compare to the OCaml topLevel. You can install it using __opam__, ```opam install utop``` and run it ```$ utop```.


### 1.2. Beyond the standard library

OCaml comes with its own libraries, the minimal system needed to run OCaml programs.Then,

- Base extends the OCaml standard library;

- Core-kernel extends Base;

- Core extends Core-kernel, notably with its Unix API.

### 1.3. The ```Hello, World``` program
The simplest, in any REPL,
```OCaml
 # print_string "Hello, World!\n";;    (* print_endline will alos fit for the \n job *)
```


**Nota Bene:** Whenever it is possible, we drop the REPL stage, since we learn programming languages to be able to run scripts and programs in standalone units, not in an interactive shell.





## 2. Building, Compiling, Running

### 2.a. Building


### 2.b. Compiling

### 2.c. Running

### 2.d. Running with command line arguments





## 3. OCaml quick cheat sheet

### 3.1. Variable, function, numeric, let in, let rec & let binding

**Numeric**
- You can insert underscores in any numeric litterals, at any place. Best place, to separate every three digits for readability, like in ```# 30_000_000.45;;```;

**Variables**
- must start with a lower case or an underscore "_",
- then any combination of characters of the alphabet characters and "_" or the prime " ' " character;

#### let binding, functions, recursive binding
- For variables, ```let x' = 3;;``` or ```let x_plus_y = 3_14.15```;
- for functions, ```let square x = x*X;;```;


### 3.2. Type inference & Infere generic type
- OCaml determines the type of an expression respect to the available type information derived from its constituents. This technique is called __type inference__:
```ocaml
# let x = 3;;
val x : int = 3
```
- In some cases, not enough information is provided, then the type cannot be deduced, then we get a __generic type__, also called __parametric polymorphism__,
```ocaml
# let first_if_true test x y =
    if test x then x else y
    ;;
  val first_if_true : ('a -> bool) -> 'a -> 'a -> 'a = <fun>
```


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
