# Good Coding Practices for programming with R Programming Language

The coding practice follows the Google's R Style Guide at: https://google.github.io/styleguide/Rguide.xml

## Exception: 
single hash is used to comment codes and double hashes are used to comment plain english sentences.

## Additions:
For calling a function defined in an external package, use `<package name>::<function name>(...)` instead of just `<function name>(...)`.

In a `for` loop, remove the loop counter object immediately after the end of the loop.
```r
for(loop.counter in pos.anchor.matrices) {
      ## do something
}
rm(loop.counter)
```

Do not depend on the operator precedence and associativity. Always use paired parentheses to manually define the precedence. 

