# OCaml_Quick_guide_and_Training
Fast getting started and cheat sheet for OCaml. Some exercices and problems with their solutions

## Set-up

### Installing OCaml
```shell
brew install ocaml
```
### Installing the package manager
```shell
brew install opam
```

### OCaml TopLevel vs UTop
When you run ```ocaml```, you enter the OCaml REPL, Read-Eval-Print-Loop. It is the TopLevel system.

UTop, the Universal TopLevel is an improved interface compare to the OCaml topLevel. You can install it using __opam__,
```shell
opam install utop
```


### Beyond the standard library
OCaml comes with its own libraries, the minimal system needed to run OCaml programs.

- Base extends the OCaml standard library;

- Core-kernel extends Base;

- Core extends Core-kernel, notably with its Unix API.


**Nota Bene:** we drop the REPL stage, since we learn programming languages to be able to run scripts and programs in standalone units, not in an interactive shell.


### OCaml type inference
Type inference is the ability of OCaml to determine the type of an expression. The type of an expression is inferred from the available type information about the components of that expression.
