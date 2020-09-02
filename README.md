# Custom programming language (lisp) created using C.
# Implements REPL (read-evaluate-print-loop) which supports the following:
  - variable declaration
  - conditionals
  - functions
  - strings
  - recursion
  - error handling
  - printing
  - comments
  - file loading (Work in Progress)
  
Compilation/Running (Ubuntu Linux):
  gcc lisp.c mpc.c  -ledit -lm -o lisp
  
  ./lisp
  
Note: Language uses polish notation (Operator comes before operands). 
e.g. + 1 2 is 1 + 2 in standard notation. More examples can be seen below.

Example commands:
 
  function defining function (allows for simpler function declaration):
  
    def {fun} (\ {args body} {def (head args) (\ (tail args) body)})
  
  list length:
   
    (fun {len l} { if (== l {}) {0} {+ 1 (len (tail l))}})

  reverse list:
  
    (fun {reverse l} { if (== l {}) {{}} {join (reverse (tail l)) (head l)}})
    
  Commands to use functions once declared:
  
    len {1 2 3 4}
  
    reverse {1 2 3 4}
