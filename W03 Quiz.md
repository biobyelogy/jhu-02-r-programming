R Programming 第三周 Quiz
===

[@生物你好生物再见](http://www.weibo.com/biobyelogy)


### Question 1
Take a look at the 'iris' dataset that comes with R. The data can be loaded with the code:
```R
library(datasets)
data(iris)
```
There will be an object called 'iris' in your workspace. In this dataset, what is the mean of 'Sepal.Length' for the species virginica? (Please only enter the numeric result and nothing else.)

> 用 `split` 函数将 `iris` 按照 `Sepal.Length` 分组，结果为一个 `list`，选出 `list` 中 `virginica` 那一组，放入 `mean` 函数。

===

### Question 2
Continuing with the 'iris' dataset from the previous Question, what R code returns a vector of the means of the variables 'Sepal.Length', 'Sepal.Width', 'Petal.Length', and 'Petal.Width'?

> 回顾 PPT 02 apply，`apply(数据集, 维度, 函数, ...)`。

===

### Question 3
Load the 'mtcars' dataset in R with the following code
```R
library(datasets)
data(mtcars)
```
There will be an object names 'mtcars' in your workspace. How can one calculate the average miles per gallon (mpg) by number of cylinders in the car (cyl)?

> 回顾 PPT 03 tapply，`tapply(数据集, 分组, 函数, ...)`。

===

### Question 4
Continuing with the 'mtcars' dataset from the previous Question, what is the absolute difference between the average horsepower of 4-cylinder cars and the average horsepower of 8-cylinder cars?

> 代码和上一题类似。得出平均值之后相减取绝对值。

===

### Question 5
If you run `debug(ls)`, what happens when you next call the 'ls' function?

> 回顾 PPT 06 debugging。注意使用 `Q` 命令退出 `browser`。



