# Custom programming language (lisp) 
  - Uses Mpc.c, a parser combinator library.
  
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
  
# Compilation/Running (Ubuntu Linux):
  
  gcc lisp.c mpc.c  -ledit -lm -o lisp
  
  ./lisp
  
# Note
  - Language uses polish notation (Operator comes before operands). 
  - e.g. + 1 2 is 1 + 2 in standard notation. More examples can be seen below.

# Example commands:
 
  function defining function (allows for simpler function declaration):
  
    def {fun} (\ {args body} {def (head args) (\ (tail args) body)})
  
  list length:
   
    (fun {len l} { if (== l {}) {0} {+ 1 (len (tail l))}})

  reverse list:
  
    (fun {reverse l} { if (== l {}) {{}} {join (reverse (tail l)) (head l)}})
    
  Commands to use functions once declared:
  
    len {1 2 3 4}
  
    reverse {1 2 3 4}
  
  Other example functions can be seen in example_functions.txt
  
  # Demo
  
  ![lisp](https://user-images.githubusercontent.com/60115853/92162867-73481e80-edf8-11ea-86e4-0fe12423ce40.png)
  
  
