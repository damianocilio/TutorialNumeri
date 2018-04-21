# Tutorial on Numbers
## This tutorial's aim is to explain how to use numbers in R language, beginning with very easy examples

When you have a vector - or a list of numbers - you can work on it, since the basic operations are already available in the memory of R. The basic operations will act on the whole vector and they can be used to quickly perform a large number of calculations with a single command.
There is one thing that has to be uderlined: if you perform an operation on more than one vector, it is often necessary that all the vectors contain the same number of elements.

Defining a vector and calling it "a", you can see how to add and subtract constant numbers from all the numbers within the vector.
If the vector contains the numbers 1, 2, 3 and 4, you will then see how to add 5 to each of the numbers, subtract 10 from each of the numbers, multiply each number by 4 and divide each number by 5.

```{r}
> a <-  c ( 1 , 2 , 3 , 4 ) 
> a
 [1] 1 2 3 4 
> a +  5 
[1] 6 7 8 9 
> a -  10 
[1] -9 -8 -7 -6 
> a * 4 
[1] 4 8 12 16 
> a / 5 
[1] 0.2 0.4 0.6 0.8
```

You can save the results of an operation in another vector called *b*:

```{r}
> b <- a -  10 
> b
 [1] -9 -8 -7 -6
```

If you want to perform a square root function, an exponential function or a logarithm function you can use the commands:

```{r}
> sqrt ( a ) 
[1] 1.000000 1.414214 1.732051 2.000000 
> exp ( a ) 
[1] 2.718282 7.389056 20.085537 54.598150 
> log ( a ) 
[1] 0.0000000 0.6931472 1.0986123 1.3862944 
> exp ( log ( a )) 
[1] 1 2 3 4
```

By combining operations and using parentheses you can write the formulas in a more complex way:
 
```{r}
> c  <-  ( a +  sqrt ( a )) / ( exp ( 2 ) +1 ) 
> c 
[1] 0.2384058 0.4069842 0.5640743 0.7152175
```


You can run the same operations on the whole vectors. For example, you can add the elements of *a* in *b*, using the following command:

```{r}
> a + b
[1] -8 -6 -4 -2
```

You can also use other operations such as:

```{r}
> a * b
 [1] -9 -16 -21 -24 
> a / b
 [1] -0.1111111 -0.2500000 -0.4285714 -0.6666667 
> ( a +3 ) / ( sqrt ( 1 - b ) * 2-1 ) 
[ 1] 0.7512364 1.0000000 1.2884234 1.6311303
```


You have to be careful about one thing: when performing operations on vectors, they are working elements by element. Therefore, it is necessary that these vectors have the same number of elements:

```{r}
> a <-  c ( 1 , 2 , 3 ) 
> b <-  c ( 10 , 11 , 12 , 13 ) 
> a + b
 [1] 11 13 15 14 
Warning message:
longer object length
        is not a multiple of shorter object length in: a + b
```

While working in R and creating new vectors, it can be easy to 
As we work in R and create new vectors, it can be easy to lose track of the variables we have defined so far. In order to get a list of all the variables which have been defined, we can use the command ```ls ()```:

```{r}
> ls () 
[1] "a" "b" "belly" "c" "last.warning" 
[6] "tree" "alberi"
```