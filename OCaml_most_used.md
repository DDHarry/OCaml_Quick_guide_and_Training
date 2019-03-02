# The not so trivial OCaml quick reminder

For the most used keywords, expressions & idioms


## OCaml system

**Getting info on the module**
- opam
```shell
opam show core_kernel
```
- opam.ocaml.org

## OCaml data structure

#### tuples
- tuples "()" are non mandatory :: ```let a_tuple = (1,"two",3.);;```
#### lists
- lists :: ```let sports = ["Fencing","Formula 1","running","swimming"];;```
- length :: ```OCaml
List.length sports;;
-: int = 4
```


## OCaml keywords

**Lists**
- List.length l

**Numerics**
- Float.of_int x  ::  conversion (__of_int__ function from the __Float__ module)

**Strings**
- String.length s


## OCaml idioms
