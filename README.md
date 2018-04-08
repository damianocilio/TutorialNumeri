# TutorialNumeri
## Questo tutorial si pone come obiettivo quello di spiegare come utilizzare i numeri nell'ambiente R partendo da esempi estremamente semplici.

Dal momento in cui si ha un vettore (o una lista di numeri), possiamo lavorare su di ess, dato che nella memoria di R sono disponibili le operazioni di base. La operazioni di base agiranno su un intero vettore e possono essere utilizzate per eseguire rapidamente un numero elevato di calcoli con un singolo comando.
C'è una cosa da notare: se si esegue un'operazione su più di un vettore è spesso necessario che tutti i vettori contengano lo stesso numero di voci.

Definiamo un vettore che chiameremo "a" e vedremo come aggiungere e sottrarre numeri costanti da tutti i numeri nel vettore. 
Il vettore conterrà i numeri 1, 2, 3 e 4. Vedremo quindi come aggiungere 5 a ciascuno dei numeri, sottrarre 10 da ciascuno dei numeri, moltiplicare ogni numero per 4 e dividere ciascun numero per 5 .

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
[1] 0,2 0,4 0,6 0,8
```
Possiamo salvare i risultati in un altro vettore chiamato *b* :

```{r}
> b <- a -  10 
> b
 [1] -9 -8 -7 -6
```
 
Se si desidera svolgere la radice quadrata, elevare a potenza ciascun numero, il logaritmo, ecc., è possibile utilizzare i comandi:
 
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
Combinando le operazioni e usando le parentesi possiamo rendere le espressioni più complesse:
 
```{r}
> c  <-  ( a +  sqrt ( a )) / ( exp ( 2 ) +1 ) 
> c 
[1] 0.2384058 0.4069842 0.5640743 0.7152175
```

E' possibile eseguire le stesse operazioni con interi vettori. Ad esempio, possiamo aggiungere gli elementi di *a* in *b*, utilizzando il seguente comando:

```{r}
> a + b
[1] -8 -6 -4 -2
```
L'operazione viene eseguita elemento per elemento. Possiamo svolgerla anche con le altre operazioni:

```{r}
> a * b
 [1] -9 -16 -21 -24 
> a / b
 [1] -0.1111111 -0.2500000 -0.4285714 -0.6666667 
> ( a +3 ) / ( sqrt ( 1 - b ) * 2-1 ) 
[ 1] 0.7512364 1.0000000 1.2884234 1.6311303
```

Dobbiamo stare attenti a una cosa. Quando si eseguono operazioni su vettori, vengono eseguite elemento per elemento. E' necessario dunque che questi abbiano lo stesso numero di elementi :

```{r}
> a <-  c ( 1 , 2 , 3 ) 
> b <-  c ( 10 , 11 , 12 , 13 ) 
> a + b
 [1] 11 13 15 14 
Warning message:
longer object length
        is not a multiple of shorter object length in: a + b
```

Mentre lavoriamo in R e creiamo nuovi vettori, può essere facile perdere traccia di quali variabili abbiamo definito. Per ottenere un elenco di tutte le variabili che sono state definite, utilizziamo il comando ```{r}ls ():```

```{r}
> ls () 
[1] "a" "b" "bubba" "c" "last.warning" 
[6] "albero" "alberi
```
