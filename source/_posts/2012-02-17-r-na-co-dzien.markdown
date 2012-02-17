---
layout: post
title: "R na co dzień"
date: 2012-02-17 17:25
comments: true
categories: [r, tools, math]
---

Możemy pracować na konsoli R albo korzystając z trybu *ESS* w Emacsie.


Polecenia, które wykonujemy codziennie:

```r
source("hello.r")
objects()
ls()

z <- read.table("http://inf.ug.edu.pl/~wbzyl/r/2x2")
z
  V1 V2
1  1  2
2  3  4

save(z)

rm(z)
rm(list = ls())

load(z)

methods(ls)
methods(class="default")

?ls

x <- c(1, 2, 3)
class(x)
  [1] "numeric"
y <- as.character(x)
  [1] "character"
class(y)
y
  [1] "1" "2" "3"
```


### Funkcje zwracające wektor

Na przykład:

```r
z12 <- function(z) return(c(z, z^2))
x = 1:4
matrix(z12(x), ncol=2)
     [,1] [,2]
[1,]    1    1
[2,]    2    4
[3,]    3    9
[4,]    4   16

z12(x)

[1]  1  2  3  4  1  4  9 16
```


## Praca w trybie wsadowym

W pliku *rnorm_hist.r* wpisano następujące instrukcje:

```r rnorm_hist.r
pdf("histogram.pdf")
hist(rnorm(1024)
graphics.off()
```

Praca w trybie wsadowym:

```sh
R --vanilla rnorm_hist.r
```
