# Good Coding Practices for programming with R Programming Language

The coding practice follows the Google's R Style Guide at: https://google.github.io/styleguide/Rguide.xml

## Exception: 
Single hash is used to comment codes and double hashes are used to comment plain english sentences. Quote the object names while referring to them inside comments.  
Example:
```r
## Find out the position of the anchor matrix
## immediately left to the current 'time.pt.idx'
left <- (time.pt.idx + num.interm.matrices.per.interval) %/% (num.interm.matrices.per.interval + 1)
```


## Additions:
### 1
For calling a function defined in an external package, use `<package name>::<function name>(...)` instead of just `<function name>(...)`.

### 2
In a `for` loop, remove the loop counter object immediately after the end of the loop.
```r
for(loop.counter in pos.anchor.matrices) {
      ## do something
}
rm(loop.counter)
```
### 3
Do not depend on the operator precedence and associativity. Always use paired parentheses to manually define the precedence. 
