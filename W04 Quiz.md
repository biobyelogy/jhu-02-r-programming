R Programming 第四周 Quiz
---

[@生物你好生物再见](http://www.weibo.com/biobyelogy)

---

### Question 1
What is produced at the end of this snippet of R code?
```R
set.seed(1)
rpois(5, 2)
```
> 运行一下即可，顺便回顾一下 `set.seed()` 的作用（PPT 01 Simulation）。

---

### Question 2
What R function can be used to generate standard Normal random variables?

> 回顾 PPT 01 Simulation，四大类型：`r`、`d`、`p`、`q`。

---

### Question 3
When simulating data, why is using the `set.seed()` function important?

> 回顾 PPT 01 Simulation。

---

### Question 4
Which function can be used to evaluate the inverse cumulative distribution function for the Poisson distribution?

> 回顾 PPT 01 Simulation 四大类型，注意是 “inverse cumulative”。

---

### Question 5
What does the following code do?
```R
set.seed(10)
x <- rbinom(10, 10, 0.5)
e <- rnorm(10, 0, 20)
y <- 0.5 + 2 * x + e
```

> 回顾 PPT 01 Simulation。

---

### Question 6
What R function can be used to generate Binomial random variables?

> 回顾 PPT 01 Simulation。

---

### Question 7
What aspect of the R runtime does the profiler keep track of when an R expression is evaluated?

> 回顾 PPT 02 Profiler。

---

### Question 8
Consider the following R code
```R
library(datasets)
Rprof()
fit <- lm(y ~ x1 + x2)
Rprof(NULL)
```
(Assume that `y`, `x1`, and `x2` are present in the workspace.) Without running the code, what percentage of the run time is spent in the `lm` function, based on the `by.total` method of normalization shown in `summaryRprof()`?

> 回顾 PPT 02 Profiler。或者使用积累多年的解题技巧。

---

### Question 9
When using 'system.time()', what is the user time?

> PPT 上讲得不是很清楚。根据 R 帮助文档，`system.time()` 在程序运行的头、尾调用两次 `proc.time()` 函数，相减得到时间差。`proc.time()` 函数结果包括：
>
- 系统时间：the CPU time charged for the execution by the system on behalf of the calling process，即执行底层系统指令所花费的 CPU 时间。
- 用户时间：the CPU time charged for the execution of user instructions of the calling process，即执行用户指令所花费的 CPU 时间。PPT 里解释为计算表达式所花费的时间。
- 流逝时间：实际消耗的时钟时间。

---

### Question 10
If a computer has more than one available processor and R is able to take advantage of that, then which of the following is true when using `system.time()`?

> 回顾 PPT 02 Profiler。