# OCaml quick guide and training

Fast getting started and cheat sheet for OCaml. Some exercices and problems with their solutions


-----------



# 1. The OCaml REPL

## 1.1. OCaml standard REPL

Installing OCaml, then, the package manager and finally running the OCaml REPL, Read-Eval-Print-Loop :
```shell
$ brew install ocaml
$ brew install opam
$ ocaml
#       (* This is the OCaml REPL prompt *)
# #quit;;
```

## 1.2. OCaml TopLevel vs UTop

When running ```ocaml```, you enter the OCaml TopLevel system, a very minimalistic REPL. But you can get UTop, the Universal TopLevel, which is an improved interface compare to the OCaml topLevel. You can install it using __opam__, ```opam install utop``` and run it ```$ utop```.
```ocaml
$ utop
utop # #help;;
utop # #quit;;
```

## 1.3. Beyond the standard library

OCaml comes with its own libraries, the minimal system needed to run OCaml programs.Then,

### Base
- Extends the OCaml standard library; Base is designed to be portable, hence the I/O functionalities are not considered (use "stdio"). The same holds for any platform dependent functionality;

### Core-kernel
- Extends Base (opam core_kernel), industrial grade. The platform independent sub-part of Core;

### Core
- Extends Core-kernel, notably with its Unix API. Industrial grade.


## 1.4. The ```Hello, World``` program
The simplest, in any REPL,
```OCaml
 # print_string "Hello, World!\n";;    (* print_endline will alos fit for the \n job *)
```


**Nota Bene:** Whenever it is possible, we drop the REPL stage, since we learn programming languages to be able to run scripts and programs in standalone units, not in an interactive shell.





---------

# 2. Building, Compiling, Running
### 2.a. Building
### 2.b. Compiling
### 2.c. Running
### 2.d. Running with command line arguments

-----------





# 3. OCaml quick cheat sheet

## 3.1. Variable, function, numeric, let in, let rec & let binding

### Numerics
- You can insert underscores in any numeric litterals, at any place. Best place, to separate every three digits for readability, like in ```# 30_000_000.45;;```;

### Variables
- must start with a lower case or an underscore "_";
- then any combination of characters of the alphabet characters and "\_" or the prime " ' " character.

### Functions
- Functions in OCaml are values, which induces the uses of the let binding :
```ocaml
 let sum_if_true test first second =
  (if test first then first else 0) + (if test second then second else 0)
  ;;
  val sum_if_true : (int -> bool) -> int -> int -> int = <fun>
  ```

### let, let .. in, let rec binding
- For variables, ```let x' = 3;;``` or ```let pi_def = 3_14.15;;```; \n
- for functions : ``` let square x = x*x;;``` ~n
- let .. in


## 3.2. Type inference & Infere generic type
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

## 3.3 OCaml data structures

### Tuples
- An ordered collection of values of different types, joined by commas. __Pattern matching__ helps extracting any of these values. These two tuples are equivalent (parentheses are not mandatory), (i) <=> (ii) :
```ocaml
(i)  let a_tuple     = (1, "two", 3.) ;;

(ii) let equiv_tuple = 1, "two", 3. ;;
```

### Lists and the list module
- Any number of items of the same type. Definition with ```[]``` or ``` :: ```. Here, (iii) <=> (iv)
```OCaml
(iii) let sports  = ["Fencing";"Formula 1";"running";"Swimming"];;

(iv)  let equiv_s = "fencing" :: "formula 1" :: "Running" :: "swimming" :: [] ;;
```
- List.length
```ocaml
List.length sports;;
: - int = 4
```
- List.map
```ocaml
List.map String.length equiv_s ;;
- : int list = [7; 9; 7; 8]
```
- concatenation ```@ ``` 
```ocaml
[1;2] @ [2;3;4] ;;
- : int list = [1; 2; 2; 3; 4]

1 :: 2 :: [] @ 2 :: 3 :: [] ;;
- : int list = [1; 2; 2; 3]
```

- head-tail, pattern-matching
```ocaml
let my_favorite_sport (my_favorite :: the_rest) =
  my_favorite
;;
Warning 8: this pattern-matching is not exhaustive.
Here is an example of a case that is not matched:
[]

my_favorite_sport ["Fencing";"Formula 1";"running";"Swimming"];;
- : string = "Fencing"
```


### match statement
The first "|" is optional
```ocaml
let my_fav_sport l_sports =
  match l_sports with
    | hd :: tl -> hd
    | []       -> "Fencing"    (* A good default *)
  ;;
  ```


### Recursive list functions
A "base case" followed by a set of "inductive cases"; a classic example :
```ocaml
let rec sum l =
  match l with
    | []     -> 0             (* base case *)
    | hd::tl -> hd + sum tl   (* inductive case *)
```
Less simple, a function to remove sequential duplicates
```ocaml
let rec remove_sequential_duplicate l =
  match l with
    | []               -> []
    | hda :: hdb :: tl ->
      if hda = hdb then remove_sequential_duplicate (hdb :: tl)
      else hda :: remove_sequential_duplicate (hdb :: tl)
;;

>> Warning issued : not exhaustive
```
the ``` _ :: [] ```, singleton-list is never matched!

A better alternative
```ocaml
let rec remove_sequential_duplicate ll =
  match ll with
    | []               -> []
    | [hd]             -> [hd]
    | hda :: (hdb :: tl) ->
      if hda = hdb then remove_sequential_duplicate (hdb :: tl)
      else hda :: remove_sequential_duplicate (hdb :: tl)
;;
```



### Option (when a value might not be present)
```ocaml

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
