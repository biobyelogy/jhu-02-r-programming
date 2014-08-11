R Programming 第二周 Quiz
===

[@生物你好生物再见](http://www.weibo.com/biobyelogy)


### Question 1
Suppose I define the following function in R
```R
cube <- function(x, n) {
    x^3
}
```
What is the result of running `cube(3)` in R after defining this function?

>  回顾 PPT 02 Functions，知识点 lazy evaluation。

===

### Question 2
The following code will produce a warning in R.
```R
x <- 1:10
if(x > 5) {
    x <- 0
}
```
Why?

> `if` 的判断条件结果唯一，不会生成一个向量。

===

### Question 
Consider the following function

```
f <- function(x) {
    g <- function(y) {
        y + z
    }
    z <- 4
    x + g(x)
}
```

If I then run in R
```
z <- 10
f(3)
```
What value is returned?

> 回顾 PPT 04 Scoping Rules，知识点 lexical scoping。变量的值和函数定义一起打包成一个 closure。自由变量的值首先取决于函数被定义时它们被赋予的值，而不是函数被调用时的值。此题中，`z` 在 `f` 被定义时已有赋值 `z <- 4` ，所以 `f` 被调用时 `z <- 10` 并不起作用。

===

### Question 4
Consider the following expression:
```R
x <- 5
y <- if(x < 3) {
    NA
} else {
    10
}
```
What is the value of 'y' after evaluating this expression?

> 回顾 PPT 01 Control Structures，`if` 结构可直接用于给变量赋值。

===

### Question 5
Consider the following R function
```
h <- function(x, y = NULL, d = 3L) {
    z <- cbind(x, d)
    if(!is.null(y))
        z <- z + y
    else
        z <- z + f
    g <- x + y / z
    if(d == 3L)
        return(g)
    g <- g + 10
    g
}
```
Which symbol in the above function is a free variable?

> 回顾 PPT 04 Scoping Rules。在函数定义中，除参数外，没有明确值的变量就是自由变量。

===

### Question 6
What is an environment in R?

> 回顾 PPT 04 Scoping Rules。

===

### Question 7
The R language uses what type of scoping rule for resolving free variables?

> 回顾 PPT 04 Scoping Rules。

===

### Question 8
How are free variables in R functions resolved?

> 回顾 PPT 04 Scoping Rules。

===

### Question 9
What is one of the consequences of the scoping rules used in R?

> 回顾 PPT 04 Scoping Rules。

===

### Question 10
In R, what is the parent frame?

> 回顾 PPT 04 Scoping Rules。