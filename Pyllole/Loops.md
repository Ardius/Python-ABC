# Cicli

_Prima di studiare i cicli e gli iteratori assicurati di conoscere le [liste](Type_List.md)._

Per ripetere una determinata azione più volte e/o su più elementi si utilizzano le istruzioni _for_ e _while_ per costruire dei _"cicli"_.

Il programma ripeterà il codice all'interno del ciclo per un numero di volte determinato da una determinata condizione.

_Ricorda, in python [l'indentazione](Indentation.md) è molto importante!_


## For

I cicli for iterano sulle liste, cioé ripetono un codice per ogni elemento all'interno di una lista.


Il seguente codice:

    for animale in ["cane", "gatto", "topo"]:              
        print ("{0} è un mammifero".format(animale))

Genera il seguente risultato:

    cane è un mammifero                                    
    gatto è un mammifero
    topo è un mammifero


I cicli for posso iterare anche dal risultato di una funzione "range".

Infatti _range(numero)_ restituisce una lista di numeri da zero al numero dato

Il codice:

    for i in range(4):
        print (i)

Scriverà:

    0                                                      
    1
    2
    3


La funzione _range_ ha anche altri paramentri opzionali.

_range(lower, upper)_ restituisce una lista di numeri dal più piccolo (lower) al più grande (upper).

_range(lower, upper, step)_ restituisce una lista di numeri dal più piccolo (lower) al più grande (upper) incrementando del valore step.

Il codice: 

    for i in range(10,30,5):
        print (i)

Scriverà:

    10                                                      
    15
    20
    25


## While

I cicli while vengono eseguiti finchè la condizione indicata viene a mancare.

    x = 0                                               
    while x < 4:
        print(x)
        x += 1  

**Nota**: La sintassi _"x += 1"_ è la versione compatta di _"x = x+1"_


---

_This work is a derivative of ["Learn X in Y minutes"](https://github.com/adambard/learnxinyminutes-docs) by [adambard](https://github.com/adambard), used under a CC BY-SA 3.0 license._