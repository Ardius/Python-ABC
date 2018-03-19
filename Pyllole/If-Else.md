# If - Else

In un programma le istruzioni vengono eseguite nell'ordine in cui sono scritte nel codice. 

Per poter eseguire una parte di questo codice solo in alcuni casi si utilizza l'istruzione di controllo  _if/else_.

_Ricorda, in python [l'indentazione](Indentation.md) è molto importante!_

La sintassi di base di _if_ è:

	if condizione:                                         
	    comandi_da_eseguire

Esiste poi la possibilità di eseguire altri comandi se la condizione non risulta soddisfatta aggiungendo l'istruzione _else_.

	if condizione:                                         
	    comandi_da_eseguire
    else:
        diversi_comandi_da_eseguire


Nel caso in cui ci siano più condizioni da valutare è possibile aggiungere _elif_ (contrazione di "else if").

	if condizione_1:                                         
	    comandi_da_eseguire
	elif condizione_2:                                         
	    comandi_da_eseguire
	elif condizione_3:                                         
	    comandi_da_eseguire
    else:
        diversi_comandi_da_eseguire

In quest'ultimo caso il "ramo" di comandi in _else_ verrà eseguito solo se nessuna delle condizioni precedentemente valutate risulterà positiva.


Un esempio in Python:

    numero=5                                         
    if numero > 10:
        print("numero è maggiore di 10")
    elif numero < 10:
        print("numero è minore di 10")
    else:
        print("numero è uguale a 10.")
    
Darà come risultato:

    some_var è minore di 10                                



---

_This work is a derivative of ["Learn X in Y minutes"](https://github.com/adambard/learnxinyminutes-docs) by [adambard](https://github.com/adambard), used under a CC BY-SA 3.0 license._