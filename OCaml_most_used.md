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
- tuples "(", ")" are non mandatory :: ```let a_tuple = (1,"two",3.);;```
#### lists
- definition :: ```let sports = ["Fencing";"Formula 1";"running";"Swimming"];;```
- length & map (always ```List.map <fun> list;;```)
```OCaml
let l = ["Fencing";"Formula 1";"running";"Swimming"];;
List.length l;;
-: int = 4

List.map String.length l;;
- : int list = [7; 9; 7; 8]
```


## OCaml keywords

**Lists**
- List.length l

**Numerics**
- Float.of_int x  ::  conversion (__of_int__ function from the __Float__ module)

**Strings**
- String.length s


## OCaml idioms
