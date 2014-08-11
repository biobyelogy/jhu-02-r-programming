R Programming 第一周 Quiz
===

[@生物你好生物再见](http://www.weibo.com/biobyelogy)


### Question 1
R was developed by statisticians working at

> 回顾 PPT 01 Overview and History of R。PPT 里只提过地点是新西兰。

===

### Question 2
The definition of free software consists of four freedoms (freedoms 0 through 3). Which of the following is NOT one of the freedoms that are part of the definition?

> 回顾 PPT 01 Overview and History of R。

===

### Question 3
In R the following are all atomic data types EXCEPT

> 回顾 PPT 03 Data Types，五种基本数据类型。

===

### Question 4
If I execute the expression `x <- 4` in R, what is the class of the object `x` as determined by the `class()` function?

> 回顾 PPT 03 Data Types，numeric 和 integer 的区别。

===

### Question 5
What is the class of the object defined by `x <- c(4, TRUE)`?

> 回顾 PPT 03 Data Types，vector 内元素类型一致。不一致时，会强制转换。

===

### Question 6
If I have two vectors `x <- c(1, 3, 5)` and `y <- c(3, 2, 10)`, what is produced by the expression `cbind(x, y)`?

> 回顾 PPT 03 Data Types，区分 `cbind` 和 `rbind`。

===

### Question 7
A key property of vectors in R is that

> 回顾 PPT 03 Data Types，上面已经提及。

===

### Question 8
Suppose I have a list defined as `x <- list(2, "a", "b", TRUE)`. What does `x[[2]]` give me?

> 回顾 PPT 04 Subsetting。这三个 subsetting operator 非常重要：
> - `[<expression>]` 返回符合 `<expression>` 的子集，类型与全集相同；
> - `[[<expression>]]` 返回符合 `<expression>` 的单个元素，类型为所得元素类型；
> - `$<name>` 返回 `<name>` 指向的单个元素，类型为所得元素类型。不接受表达式。

===

### Question 9
Suppose I have a vector `x <- 1:4` and `y <- 2:3`. What is produced by the expression `x + y`?

> 在 RStudio console 试验一下即可，结论要记住。

===

### Question 10
Suppose I have a vector `x <- c(17, 14, 4, 5, 13, 12, 10)` and I want to set all elements of this vector that are greater than 10 to be equal to `4`. What R code achieves this?

> - `[<expression>]` 返回符合 `<expression>` 的子集；
> - `==` 是逻辑判断符号，`<-` 或者 `=` 才是赋值。

===

### Question 11
In the dataset provided for this Quiz, what are the column names of the dataset?

> - 写代码之前注意当前 `working directory`，可用函数 `setwd 设置；
> - 函数 `read.csv`；
> - 函数 `colnames`；
> - 答案其实后面的题干里有……

===

### Question 12
Extract the first 2 rows of the data frame and print them to the console. What does the output look like?

> 函数 `head`。

===

### Question 13
How many observations (i.e. rows) are in this data frame?

> - 函数 `nrow`；
> - 答案其实下一题选项里也有……

===

### Question 14
Extract the last 2 rows of the data frame and print them to the console. What does the output look like?

> 函数 `tail`。

===

### Question 15
What is the value of `Ozone` in the 47th row?

> 先选出 `Ozone`，再选出第 47 个数据。

===

### Question 16
How many missing values are in the `Ozone` column of this data frame?

> 此题方法很多，这里举两个。
> 方法一：
> - 用函数 `na.omit` 得到去除 `NA` 后的 `data$Ozone` 向量。
> - 用函数 `length` 得到向量内元素个数，和包含 `NA` 的 `Ozone` 向量长度相比较。
>
> 方法二：
> - 先选出 `Ozone`；
> - 用函数 `is.na` 得到一个 `Ozone` 中是否是 `NA` 的 `logical` 向量；
> - 向量中，`TRUE` 相当于 `1`，`FALSE` 相当于 `0`，用 `sum` 求和得到 `TRUE` 总数。

===

### Question 17
What is the mean of the `Ozone` column in this dataset? Exclude missing values (coded as `NA`) from this calculation.

> 函数 `mean` 有一个选项 `na.rm = T`，可在计算时去除 `NA` 元素。

===

### Question 18
Extract the subset of rows of the data frame where `Ozone` values are above `31` and `Temp` values are above `90`. What is the mean of `Solar.R` in this subset?

> 此题有很多方法：
> 方法一：
> - 用条件 `data$Ozone > 31 & data$Temp > 90` 选出所需的 `data$Solar`；
> - 注意 `&` 和 `&&` 的区别，前者返回一个向量，后者返回单一 `logical` 值，所以这里必须用 `&`；
> - 调用函数 `mean`。
>
> 方法二：
> - 用函数 `subset` 选出所需的 `Solar` 数据；
> - 调用函数 `mean`。

===

### Question 19
What is the mean of `Temp` when `Month` is equal to `6`?

> 参照上题。注意 `==` 是逻辑判断符，`=` 是赋值符号，这里必须用前者。

===

### Question 20
What was the maximum `ozone` value in the month of May (i.e. `Month = 5`)?

> 参照上题。

