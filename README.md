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

- Base extends the OCaml standard library; Base is designed to be portable, hence the I/O functionalities are not considered (use "stdio"). The same holds for any platform dependent functionality;

- Core-kernel extends Base (opam core_kernel), industrial grade. The platform independent sub-part of Core;

- Core extends Core-kernel, notably with its Unix API. Industrial grade.

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

** • Numeric**
\- You can insert underscores in any numeric litterals, at any place. Best place, to separate every three digits for readability, like in ```# 30_000_000.45;;```;

• Variables
\- must start with a lower case or an underscore "_",
\- then any combination of characters of the alphabet characters and "_" or the prime " ' " character;

• Functions
\- Functions in OCaml are values, which induces the uses of the let binding :
```ocaml
 let sum_if_true test first second =
  (if test first then first else 0) + (if test second then second else 0)
  ;;
  val sum_if_true : (int -> bool) -> int -> int -> int = <fun>
  ```

#### let, let .. in, let rec binding
\- For variables, ```let x' = 3;;``` or ```let pi_def = 3_14.15;;```;
\- for functions : ``` let square x = x*x;;```
\- let .. in


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

### 3.3 OCaml data structures

#### Tuples
- An ordered collection of values of different types, joined by commas. __Pattern matching__ helps extracting any of these values. These twi tuples are equivalent (parentheses are not mandatory) :
```ocaml
let a_tuple = (1, "two", 3.) ;;

let another_tuple = 1,"two",3. ;;
```

**Lists**
- Any number of items of the same type :
```OCaml
let sports = ["Fencing","Formula 1","swwimming"];;
```








## 6. Object Oriented programming in OCaml
Why?
- One example of use :
- Followed by "How to make it functional"? > OO needless, right?
## R. Some references: books
### R.1. Getting some help
Of course, OCaml's website is the primary source of information.
### R.2. Some books
• _Real Worrld OCaml_
